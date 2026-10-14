---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses another option of a poll they voted in",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Poll options",
            "Poll results"
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
      "text": "The Product moves the vote to the new option",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "vote",
          "effect": "changes",
          "facts": [
            "Option chosen"
          ]
        },
        {
          "entity": "post",
          "effect": "changes",
          "facts": [
            "Poll results"
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

# Change a vote

## Trigger

A User changes their mind on a poll.

## Outcome

The vote counts for the new option instead.
