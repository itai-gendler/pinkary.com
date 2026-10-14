---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest opens a channel",
      "kind": "actor",
      "actor": "guest",
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
          "place": "web::public::channel"
        }
      }
    }
  ]
}
---

# A Guest opens a channel

## Trigger

A Guest follows a channel badge.

## Outcome

The Guest sees the channel name, its post count and its posts.
