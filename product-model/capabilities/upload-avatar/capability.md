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
      "target": "app/Http/Controllers/UserAvatarController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Jobs/UpdateUserAvatar.php"
    }
  ]
}
---

# Upload avatar

A User uploads their own profile photo.
