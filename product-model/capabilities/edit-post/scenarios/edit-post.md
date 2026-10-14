---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses Edit Post on a post less than a day old, changes its text or channel and sends",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Content",
            "Channel",
            "Published at"
          ]
        },
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
          "place": "web::signed-in::post"
        }
      }
    },
    {
      "text": "The Product saves the post, moves it between channels and removes its likes",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "effect": "changes",
          "facts": [
            "Content",
            "Channel",
            "Edited at"
          ]
        },
        {
          "entity": "channel",
          "effect": "changes",
          "facts": [
            "Post count"
          ]
        },
        {
          "entity": "like",
          "effect": "removes"
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

# Edit a post

## Trigger

A User wants to fix a recent post.

## Outcome

The post shows the new text and channel, its likes are cleared, and both channels' counts follow the move.
