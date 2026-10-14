---
{
  "availability": [
    {
      "place": "web::public"
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
      "target": "resources/views/auth/two-factor-challenge.blade.php"
    }
  ]
}
---

# Complete two-factor challenge

A Guest whose password was accepted finishes logging in with a code from their authenticator app or a recovery code.
