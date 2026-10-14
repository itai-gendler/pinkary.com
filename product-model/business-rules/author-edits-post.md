---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "post",
      "effect": "changes",
      "facts": [
        "Content",
        "Channel"
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

# Only the author edits a post

A post's text, images and channel change only through its author.
