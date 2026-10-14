---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest opens an answered question's page",
      "kind": "actor",
      "actor": "guest",
      "entities": [
        {
          "entity": "question",
          "effect": "reads",
          "facts": [
            "Question text",
            "Anonymous",
            "Answer",
            "Answered at",
            "Views"
          ]
        },
        {
          "entity": "comment",
          "effect": "reads",
          "facts": [
            "Content",
            "Published at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::post"
        }
      }
    }
  ]
}
---

# A Guest reads an answered question

## Trigger

A Guest opens an answer link.

## Outcome

The Guest sees the question, the answer and the comments; an anonymous asker stays hidden.
