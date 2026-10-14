---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "question"
    },
    {
      "type": "entity",
      "id": "post"
    },
    {
      "type": "entity",
      "id": "comment"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Models/Scopes/WhereNotModerated.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Observers/QuestionObserver.php#deleted"
    }
  ]
}
---

# Ignored and reported questions and deleted posts and comments are shown nowhere

Profiles, feeds, channels, hashtags, post pages and notifications leave them out, and deleting a post, answer or comment removes its comments, the later posts of its thread, its reposts and its notifications.
