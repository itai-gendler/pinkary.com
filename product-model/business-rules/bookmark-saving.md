---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "bookmark",
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
      "target": "app/Actions/Questions/CreateBookmark.php"
    }
  ]
}
---

# Only a User with a verified email bookmarks

Bookmarks are private to the User who saved them.
