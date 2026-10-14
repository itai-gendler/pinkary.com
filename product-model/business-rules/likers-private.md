---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "like",
      "effect": "reads"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "has",
          "entity": "post"
        },
        {
          "verb": "writes",
          "entity": "user"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "has",
          "entity": "question"
        },
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
      "target": "app/Policies/QuestionPolicy.php#viewLikes"
    }
  ]
}
---

# Only the owner of a post or answer sees who liked it

Everyone else sees only the number of likes.
