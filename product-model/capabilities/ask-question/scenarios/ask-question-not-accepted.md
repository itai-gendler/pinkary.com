---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens another User's profile to ask",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    },
    {
      "text": "The recipient accepts questions from no one, or only from people they follow and they do not follow this User",
      "kind": "condition",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Who can ask questions"
          ]
        },
        {
          "entity": "question",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "follow",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    },
    {
      "text": "The Product shows that the recipient is not accepting questions instead of the question form",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "question",
          "effect": "reads",
          "facts": []
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

# Recipient does not accept the question

## Trigger

A User opens the profile of someone who takes questions from no one, or only from people they follow.

## Outcome

The User is told the recipient is not accepting questions from them and cannot ask.
