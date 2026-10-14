---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses Delete on their post on the channel page and confirms",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Content",
            "Channel"
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
          "place": "web::signed-in::channel"
        }
      }
    },
    {
      "text": "The Product deletes the post and lowers the channel's post count",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "effect": "changes",
          "from": "Published",
          "to": "Deleted",
          "facts": []
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

# Delete a post from its channel page

## Trigger

A User deletes their post while on its channel's page.

## Outcome

The post is gone and the channel counts one post fewer.
