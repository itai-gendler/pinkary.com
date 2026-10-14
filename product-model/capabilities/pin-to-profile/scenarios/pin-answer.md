---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses Pin on an answered question",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "question",
          "effect": "reads",
          "facts": [
            "Question text",
            "Pinned"
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
      "text": "The Product unpins whatever was pinned and pins the question",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "question",
          "effect": "changes",
          "facts": [
            "Pinned"
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

# Pin an answered question

## Trigger

A User is proud of an answer.

## Outcome

The answered question is first on the profile.
