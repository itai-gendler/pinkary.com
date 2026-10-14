---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User writes an update and enters a new channel name",
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
      "text": "The Product creates the channel",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "channel",
          "effect": "creates",
          "facts": [
            "Name",
            "Address",
            "Post count"
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
      "text": "The Product publishes the post in the new channel",
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
          "effect": "reads",
          "facts": []
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

# Publish in a new channel

## Trigger

A User's post fits a topic no channel covers yet.

## Outcome

The channel exists with this post in it and the channel's post count is one.
