---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Services/Accounts.php#Accounts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Http/Controllers/Auth/AuthenticatedSessionController.php"
    }
  ]
}
---

# Log out

A User logs out of the account they are using; if other accounts remain in the switcher, the Product switches to one of them.
