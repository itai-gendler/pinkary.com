---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User saves new text for an old answer",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::post"
        }
      }
    },
    {
      "text": "The answer was given more than 24 hours ago",
      "kind": "condition",
      "actor": "user",
      "entities": [
        {
          "entity": "question",
          "effect": "reads",
          "facts": [
            "Answered at"
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

# Answer older than a day

## Trigger

A User tries to edit an answer given more than 24 hours ago.

## Outcome

The answer stays as it is and the User is told it can no longer be edited.
