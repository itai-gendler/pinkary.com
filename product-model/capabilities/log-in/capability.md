---
{
  "availability": [
    {
      "place": "web::public"
    },
    {
      "place": "web::signed-in"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "routes/auth.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Providers/FortifyServiceProvider.php"
    }
  ]
}
---

# Log in

A person logs in with their email and password. Signed in already, they add another existing account to the account switcher the same way.
