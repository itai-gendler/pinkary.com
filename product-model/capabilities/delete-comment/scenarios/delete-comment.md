---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses Delete on their comment and confirms",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "comment",
          "as": "deleted-comment",
          "effect": "reads",
          "facts": [
            "Content"
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
      "text": "The Product deletes the comment and removes the replies under it",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "comment",
          "as": "deleted-comment",
          "effect": "changes",
          "from": "Published",
          "to": "Deleted",
          "facts": []
        },
        {
          "entity": "comment",
          "as": "reply",
          "effect": "removes",
          "from": "Published"
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

# Delete a comment

## Trigger

A User regrets a comment.

## Outcome

The comment and the replies under it are shown nowhere.
