---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "like",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "gives",
          "entity": "user"
        }
      ]
    },
    {
      "actors": [
        "user"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Policies/LikePolicy.php"
    }
  ]
}
---

# Only the User who liked takes the like back, and an edit clears likes

The author's edit of the liked text also removes its likes.
