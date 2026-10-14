---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "bookmark",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "saves",
          "entity": "user"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Policies/BookmarkPolicy.php"
    }
  ]
}
---

# Only the User who saved a bookmark removes it

Bookmarks belong to their User.
