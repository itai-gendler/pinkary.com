---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "post",
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

# Only the author deletes a post

Deleting is the author's alone.
