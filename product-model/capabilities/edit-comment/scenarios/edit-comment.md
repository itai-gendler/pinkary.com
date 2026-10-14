---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User edits a comment less than a day old and sends it",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "comment",
          "effect": "reads",
          "facts": [
            "Content",
            "Published at"
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
      "text": "The Product saves the comment and removes its likes",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "comment",
          "effect": "changes",
          "facts": [
            "Content",
            "Edited at"
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

# Edit a comment

## Trigger

A User wants to fix a recent comment.

## Outcome

The comment shows the new text and its likes are cleared.
