---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest opens a page of something not answered, or ignored, reported or deleted",
      "kind": "actor",
      "actor": "guest",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::post"
        }
      }
    },
    {
      "text": "The question is not answered, or is ignored or reported",
      "kind": "condition",
      "actor": "guest",
      "entities": [
        {
          "entity": "question",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::post"
        }
      }
    }
  ]
}
---

# Post not available

## Trigger

Someone opens an unanswered question of another User, or anything ignored, reported or deleted.

## Outcome

The page is not found.
