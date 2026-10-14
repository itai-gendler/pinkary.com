---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses Delete on one of their answers and confirms",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "question",
          "effect": "reads",
          "facts": [
            "Question text",
            "Answer"
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
      "text": "The Product hides the question and removes its notifications",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "question",
          "effect": "changes",
          "from": "Answered",
          "to": "Ignored",
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
    },
    {
      "text": "The Product removes the comments under it",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "comment",
          "effect": "removes",
          "from": "Published"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    },
    {
      "text": "The Product removes its reposts",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "repost",
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

# Delete an answered question

## Trigger

A User no longer wants an answer on their profile.

## Outcome

The question and answer are shown nowhere; their comments, reposts and notifications are removed.
