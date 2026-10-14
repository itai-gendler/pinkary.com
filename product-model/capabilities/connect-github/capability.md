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
      "target": "app/Http/Controllers/UserGitHubUsernameController.php#UserGitHubUsernameController"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Services/GitHub.php"
    }
  ]
}
---

# Connect GitHub

A User connects their GitHub account; if that account sponsors Pinkary, the User becomes verified.
