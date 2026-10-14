---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "user",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "self": true
    },
    {
      "unattended": true,
      "when": [
        {
          "fact": "Email verified at",
          "absent": true
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Console/Commands/DeleteNonEmailVerifiedUsersCommand.php"
    }
  ]
}
---

# Only the User deletes their account, and the Product removes accounts never verified

A User deletes their own account with their password. The Product removes an account only while its email is unverified, a day after it last changed, and only when it has no links, questions or posts older than a day.
