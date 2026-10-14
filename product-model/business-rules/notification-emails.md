---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "email-unread-notifications"
    },
    {
      "type": "entity",
      "id": "notification",
      "facts": [
        "Emailed at"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Console/Commands/SendUnreadNotificationEmailsCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "routes/console.php"
    }
  ]
}
---

# Unread notifications are emailed at 13:00, daily or on Mondays, and each at most once every 30 days

Users choosing Never get no email, and addresses suppressed after bouncing are skipped.
