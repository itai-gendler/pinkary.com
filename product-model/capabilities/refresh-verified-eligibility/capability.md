---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "settings",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Http/Controllers/UserIsVerifiedController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Jobs/SyncVerifiedUser.php"
    }
  ]
}
---

# Refresh verified eligibility

A User whose connected GitHub account just started sponsoring Pinkary asks the Product to check again.
