---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "question",
      "effect": "changes",
      "to": "Reported"
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
      "target": "app/Policies/QuestionPolicy.php#update"
    }
  ]
}
---

# Only the recipient reports a question

A question is reported by the User it was asked to, before answering it.
