---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses the option they voted for",
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
      "text": "The Product removes the vote",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "vote",
          "effect": "removes"
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

# Take back a vote

## Trigger

A User chooses the option they already voted for.

## Outcome

The User has no vote in the poll.
