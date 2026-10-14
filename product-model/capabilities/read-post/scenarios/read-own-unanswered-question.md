---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens an unanswered question asked to them",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "question",
          "effect": "reads",
          "facts": [
            "Question text",
            "Anonymous",
            "Asked at"
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

# The recipient opens an unanswered question

## Trigger

A User opens a question asked to them from a notification.

## Outcome

The User sees the question with the form to answer it.
