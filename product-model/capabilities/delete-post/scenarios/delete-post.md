---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses Delete on their post and confirms",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "as": "deleted-post",
          "effect": "reads",
          "facts": [
            "Content"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    },
    {
      "text": "The Product deletes the post and removes its notifications",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "as": "deleted-post",
          "effect": "changes",
          "from": "Published",
          "to": "Deleted",
          "facts": []
        },
        {
          "entity": "notification",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    },
    {
      "text": "The Product removes the comments under it",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "comment",
          "effect": "removes",
          "from": "Published"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    },
    {
      "text": "The Product removes the later posts of its thread",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "as": "later-post",
          "effect": "removes",
          "from": "Published"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    },
    {
      "text": "The Product removes its reposts",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "repost",
          "effect": "removes"
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

# Delete a post

## Trigger

A User regrets a post.

## Outcome

The post is shown nowhere and its comments, later thread posts, reposts and notifications are removed.
