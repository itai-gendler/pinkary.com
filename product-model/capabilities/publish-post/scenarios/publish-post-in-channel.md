---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User writes an update on a channel's page, keeping that channel",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "channel",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::channel"
        }
      }
    },
    {
      "text": "The Product publishes the post in the channel and counts it",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "effect": "creates",
          "to": "Published",
          "facts": [
            "Content",
            "Published at",
            "Channel"
          ]
        },
        {
          "entity": "channel",
          "effect": "changes",
          "facts": [
            "Post count"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::channel"
        }
      }
    }
  ]
}
---

# Publish in an existing channel

## Trigger

A User shares a post from a channel's page or picks a channel.

## Outcome

The post is in the channel and the channel counts one more post.
