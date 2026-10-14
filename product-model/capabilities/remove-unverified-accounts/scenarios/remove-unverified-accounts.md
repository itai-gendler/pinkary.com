---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The hourly check finds a User whose email is unverified, unchanged for a day and with nothing on their profile older than a day",
      "kind": "condition",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Email verified at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::verify-email"
        }
      },
      "unattended": true
    },
    {
      "text": "The Product deletes the User",
      "kind": "product",
      "entities": [
        {
          "entity": "user",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::verify-email"
        }
      }
    }
  ]
}
---

# Remove an unverified account

## Trigger

The hourly check finds an account unverified for more than a day.

## Outcome

The account is gone and its username and email are free again.
