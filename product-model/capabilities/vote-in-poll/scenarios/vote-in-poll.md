---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses an option of an open poll",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Poll options",
            "Poll ends"
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
      "text": "The Product records the vote and counts it",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "vote",
          "effect": "creates",
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

# Vote in a poll

## Trigger

A User has an opinion on a poll.

## Outcome

The vote counts for the chosen option and the User sees the results.
