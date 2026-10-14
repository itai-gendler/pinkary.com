---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "comment",
      "effect": "changes",
      "facts": [
        "Content"
      ]
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
      "target": "app/Policies/QuestionPolicy.php#update"
    }
  ]
}
---

# Only the author edits a comment

A comment's text changes only through its author.
