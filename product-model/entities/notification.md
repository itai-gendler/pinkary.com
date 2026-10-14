---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Notifications/QuestionCreated.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Http/Controllers/NotificationController.php"
    }
  ]
}
---

# Notification

Something that happened for a User: a new question, an answer to their question, a comment on their post, a mention, a new follower or a repost.

## Information kept

- **Kind** — new question or comment, answer, mention, new follower or repost
- **Subject** — the question, post, comment or follower it is about
- **Received at** — when it was created
- **Emailed at** — when it was last included in an email of unread notifications
