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
      "target": "app/Http/Controllers/UserAvatarController.php#UserAvatarController"
    }
  ]
}
---

# Delete uploaded avatar

A User drops their uploaded avatar, or asks for a fresh one, and the Product fetches one from their connected GitHub account or from Gravatar.
