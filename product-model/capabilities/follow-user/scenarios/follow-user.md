---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses Follow on another User's profile",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Name",
            "Username"
          ]
        },
        {
          "entity": "follow",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    },
    {
      "text": "The Product records the follow and notifies the followed User",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "follow",
          "effect": "creates",
          "to": "Following",
          "facts": []
        },
        {
          "entity": "notification",
          "effect": "creates",
          "facts": [
            "Kind",
            "Subject",
            "Received at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    }
  ]
}
---

# Follow a User

## Trigger

A User wants to see someone's posts.

## Outcome

The User follows them, sees their posts in Following, and the followed User is notified.
