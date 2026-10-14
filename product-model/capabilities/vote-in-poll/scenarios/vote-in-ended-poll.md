---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses an option",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Poll options"
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
      "text": "The poll has ended",
      "kind": "condition",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Poll ends"
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

# Poll has ended

## Trigger

A User votes after the poll closed.

## Outcome

Nothing changes and the User is told voting is over.
