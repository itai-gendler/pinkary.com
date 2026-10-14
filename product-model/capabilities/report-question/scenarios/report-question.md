---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses Report on an unanswered question and confirms",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "question",
          "effect": "reads",
          "facts": [
            "Question text"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    },
    {
      "text": "The Product marks the question reported and removes its notifications",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "question",
          "effect": "changes",
          "from": "Unanswered",
          "to": "Reported",
          "facts": []
        },
        {
          "entity": "notification",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    }
  ]
}
---

# Report a question

## Trigger

A User receives an abusive question.

## Outcome

The question is reported, shown nowhere, and its notifications are gone.
