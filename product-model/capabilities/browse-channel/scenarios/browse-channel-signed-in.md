---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens a channel",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "channel",
          "effect": "reads",
          "facts": [
            "Name",
            "Post count"
          ]
        },
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Content",
            "Images",
            "Published at",
            "Poll options",
            "Poll results",
            "Channel",
            "Views"
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

# A User opens a channel

## Trigger

A User wants posts on a topic.

## Outcome

The User sees the channel's posts and can post in it.
