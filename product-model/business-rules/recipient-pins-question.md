---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "question",
      "effect": "changes",
      "facts": [
        "Pinned"
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
      "target": "app/Policies/QuestionPolicy.php#pin"
    }
  ]
}
---

# Only the recipient pins or unpins an answered question

The recipient may pin a question once it is answered.
