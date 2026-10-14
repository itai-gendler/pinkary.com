---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "user",
      "effect": "changes",
      "facts": [
        "Verified",
        "Company verified"
      ]
    }
  ],
  "permits": [
    {
      "self": true
    },
    {
      "unattended": true
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Jobs/SyncVerifiedUser.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Models/User.php#getIsVerifiedAttribute"
    },
    {
      "kind": "code",
      "role": "intent",
      "target": "resources/views/profile/partials/verified-form.blade.php"
    }
  ]
}
---

# The verified badges follow the User's GitHub sponsorship of Pinkary

A User is verified while their connected GitHub account sponsors Pinkary, and company verified while it sponsors as a company; the badges are checked when the User connects, disconnects or refreshes, and daily by the Product. The sponsor lists in configuration also grant the badges.
