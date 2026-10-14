---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens a notification about an answer, comment, mention or repost",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "notification",
          "effect": "reads",
          "facts": [
            "Kind",
            "Subject"
          ]
        },
        {
          "entity": "comment",
          "effect": "reads",
          "facts": [
            "Content"
          ]
        },
        {
          "entity": "repost",
          "effect": "reads",
          "facts": [
            "Reposted at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::notifications"
        }
      }
    },
    {
      "text": "The Product clears the notification and opens the post's page",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "notification",
          "effect": "removes"
        },
        {
          "entity": "post",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::post"
        }
      }
    }
  ]
}
---

# Open an answer, comment, mention or repost notification

## Trigger

A User wants to see what happened.

## Outcome

The notification is cleared and the User is on the page of the post or answer.
