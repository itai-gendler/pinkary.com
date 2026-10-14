---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "question",
      "effect": "reads"
    }
  ],
  "permits": [
    {
      "actors": [
        "guest",
        "user"
      ],
      "when": [
        {
          "state": "Answered"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "receives",
          "entity": "user"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Policies/QuestionPolicy.php#view"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Queries/Feeds/UserQuestionsFeed.php"
    }
  ]
}
---

# An unanswered question is read only by its recipient

Everyone reads answered questions; until it is answered, a question is visible only to the User it was asked to.
