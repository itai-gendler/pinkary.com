---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "question",
      "effect": "changes",
      "to": "Ignored"
    }
  ],
  "permits": [
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
      "target": "app/Policies/QuestionPolicy.php#ignore"
    }
  ]
}
---

# Only the recipient ignores or deletes a question

Ignoring an unanswered question and deleting an answered one hide it for good.
