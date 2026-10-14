---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "notification",
      "effect": "reads"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "receives",
          "entity": "user"
        }
      ]
    },
    {
      "unattended": true
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Http/Controllers/NotificationController.php"
    }
  ]
}
---

# Only the recipient reads their notifications

Notification emails go to the recipient only.
