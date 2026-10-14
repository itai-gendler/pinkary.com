---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "comment",
      "effect": "changes",
      "to": "Deleted"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "writes",
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

# Only the author deletes a comment

Deleting a comment is its author's alone.
