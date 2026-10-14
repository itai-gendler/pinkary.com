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
      "target": "app/Http/Controllers/Auth/VerifyEmailController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Http/Controllers/Auth/EmailVerificationNotificationController.php"
    }
  ]
}
---

# Verify email

A User confirms their email address through the link emailed to them, or asks for a new link.
