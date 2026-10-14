---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The scheduled run reaches a User whose mail preference matches and who has unread notifications not emailed in the last 30 days",
      "kind": "condition",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Mail preference",
            "Email"
          ]
        },
        {
          "entity": "notification",
          "effect": "reads",
          "facts": [
            "Emailed at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::notifications"
        }
      },
      "unattended": true
    },
    {
      "text": "The Product records the notifications as emailed and emails the unread count",
      "kind": "product",
      "entities": [
        {
          "entity": "notification",
          "effect": "changes",
          "facts": [
            "Emailed at"
          ]
        },
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Email",
            "Name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::notifications"
        }
      }
    }
  ]
}
---

# Email the unread notifications

## Trigger

It is 13:00 on any day for Daily Users, or on Monday for Weekly Users.

## Outcome

Each such User with notifications not emailed in the last 30 days gets one email with their unread count.

## Edge cases

- Users whose email is suppressed after bouncing get no email.
