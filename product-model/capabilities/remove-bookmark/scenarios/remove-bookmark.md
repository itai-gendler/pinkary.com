---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User removes the bookmark on a post in their bookmarks",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Content"
          ]
        },
        {
          "entity": "bookmark",
          "effect": "reads",
          "facts": [
            "Bookmarked at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::bookmarks"
        }
      }
    },
    {
      "text": "The Product removes the bookmark",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "bookmark",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::bookmarks"
        }
      }
    }
  ]
}
---

# Remove a bookmark

## Trigger

A User is done with a bookmarked post.

## Outcome

The post leaves the User's bookmarks.
