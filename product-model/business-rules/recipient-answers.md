---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "question",
      "effect": "changes",
      "facts": [
        "Answer"
      ]
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

# Only the recipient answers a question or edits the answer

The User a question was asked to is the only one who answers it.
