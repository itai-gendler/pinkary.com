---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User writes up to 255 characters on another User's profile, keeps or changes the anonymous choice, and sends it",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Ask anonymously by default",
            "Who can ask questions"
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
      "text": "The Product creates the question and notifies the recipient",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "question",
          "effect": "creates",
          "to": "Unanswered",
          "facts": [
            "Question text",
            "Anonymous",
            "Asked at"
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
          "place": "web::signed-in::profile"
        }
      }
    }
  ]
}
---

# Ask a question

## Trigger

A User is curious about someone.

## Outcome

The question waits unanswered for the recipient, who is notified; the asker stays hidden when it is anonymous.
