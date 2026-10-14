---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User writes an answer and sends it",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "question",
          "effect": "reads",
          "facts": [
            "Question text",
            "Anonymous"
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
      "text": "The Product saves the answer and notifies the asker",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "question",
          "effect": "changes",
          "from": "Unanswered",
          "to": "Answered",
          "facts": [
            "Answer",
            "Answered at"
          ]
        },
        {
          "entity": "notification",
          "effect": "creates",
          "facts": [
            "Kind",
            "Subject",
            "Received at"
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

# Answer from the question's page

## Trigger

A User opened a question asked to them on its own page.

## Outcome

The answer is public and the asker is notified.
