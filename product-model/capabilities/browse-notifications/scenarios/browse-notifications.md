---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens Notifications",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "notification",
          "effect": "reads",
          "facts": [
            "Kind",
            "Subject",
            "Received at"
          ]
        },
        {
          "entity": "question",
          "effect": "reads",
          "facts": [
            "Question text",
            "Anonymous"
          ]
        },
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Content"
          ]
        },
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Name",
            "Username",
            "Avatar"
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

# Browse notifications

## Trigger

A User sees they have new notifications.

## Outcome

The User sees each notification with the question, post, comment, follower or repost it is about.
