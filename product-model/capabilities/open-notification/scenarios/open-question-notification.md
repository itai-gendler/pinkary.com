---
{
  "kind": "primary",
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
      "contexts": {
        "web": {
          "place": "web::signed-in::notifications"
        }
      }
    },
    {
      "text": "The question is not answered yet, so the notification stays",
      "kind": "condition",
      "actor": "user",
      "entities": [
        {
          "entity": "question",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "notification",
          "effect": "reads",
          "facts": []
        }
      ],
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
      "contexts": {
        "web": {
          "place": "web::signed-in::post"
        }
      }
    }
  ]
}
---

# Open a new-question notification

## Trigger

A User wants to answer a question they were asked.

## Outcome

The User is on the question's page; the notification stays until the question is answered.
