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
      "target": "app/Actions/Users/UpdateUser.php"
    }
  ]
}
---

# Edit profile

A User saves their profile information: name, username, email, bio, how often unread notifications are emailed, the default feed, whether questions they ask start anonymous, and who can ask them questions.
