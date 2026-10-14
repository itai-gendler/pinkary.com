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
      "target": "app/Http/Controllers/UserController.php#UserController"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Models/User.php#purge"
    }
  ]
}
---

# Delete account

A User permanently deletes their account after entering their password, with everything they asked, answered and posted.
