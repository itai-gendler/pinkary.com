---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User hearts a post in a feed",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Content"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::home"
        }
      }
    },
    {
      "text": "The Product records the like",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "like",
          "effect": "creates",
          "facts": [
            "Liked at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::home"
        }
      }
    }
  ]
}
---

# Like a post

## Trigger

A User enjoys a post.

## Outcome

The post counts one more like, shown as liked to this User.

## Edge cases

- Liking something already liked changes nothing.
