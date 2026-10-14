---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User writes an answer of up to 1000 characters and sends it",
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
          "place": "web::signed-in::profile"
        }
      }
    },
    {
      "text": "The Product saves the answer, records its hashtags and notifies the asker and the mentioned Users",
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
          "entity": "hashtag",
          "effect": "creates",
          "facts": [
            "Name"
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

# Answer a question

## Trigger

A User has an unanswered question on their profile.

## Outcome

The answer is public on the profile and in the feeds; the asker and anyone mentioned are notified, and the recipient's notification of the question is cleared.
