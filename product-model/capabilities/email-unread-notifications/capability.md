---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "notifications",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Console/Commands/SendUnreadNotificationEmailsCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Mail/PendingNotifications.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "routes/console.php"
    }
  ]
}
---

# Email unread notifications

The Product emails each User a count of their unread notifications, daily or on Mondays depending on their mail preference.
