---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User hearts an answered question",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "question",
          "effect": "reads",
          "facts": [
            "Question text",
            "Answer"
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
          "place": "web::signed-in::post"
        }
      }
    }
  ]
}
---

# Like an answer

## Trigger

A User enjoys an answer.

## Outcome

The answered question counts one more like.
