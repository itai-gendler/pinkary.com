---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "like",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "actors": [
        "user"
      ],
      "when": [
        {
          "entity": "user",
          "fact": "Email verified at",
          "present": true
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Actions/Questions/CreateLike.php"
    }
  ]
}
---

# Only a User with a verified email likes

Each User likes a thing at most once.
