---
{
  "kind": "primary",
  "result": "achieved",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens a notification about a new question",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "notification",
          "effect": "reads",
          "facts": [
            "Kind",
            "Subject"
          ]
        },
        {
          "entity": "question",
          "effect": "reads",
          "facts": [
            "Question text"
          ]
        }
      ],
      "capability": "open-notification",
      "contexts": {
        "web": {
          "place": "web::signed-in::notifications"
        }
      }
    },
    {
      "text": "The Product opens the question's page",
      "kind": "product",
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
      "capability": "open-notification",
      "contexts": {
        "web": {
          "place": "web::signed-in::post"
        }
      }
    },
    {
      "text": "The User writes an answer and sends it",
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
      "capability": "answer-question",
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
      "capability": "answer-question",
      "contexts": {
        "web": {
          "place": "web::signed-in::post"
        }
      }
    }
  ]
}
---

# Open the notification and answer

## Trigger

A User is notified of a new question.

## Outcome

The question is answered.
