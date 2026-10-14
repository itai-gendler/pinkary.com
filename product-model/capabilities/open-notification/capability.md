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
      "target": "app/Http/Controllers/NotificationController.php#show"
    }
  ]
}
---

# Open notification

A User opens a notification and is taken to what it is about; opening it clears it, except a new question, which stays until answered.
