---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "post",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "actors": [
        "user"
      ],
      "when": [
        {
          "entity": "user",
          "fact": "Email verified at",
          "present": true
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Livewire/Concerns/NeedsVerifiedEmail.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Http/Middleware/EnsureVerifiedEmailsForSignInUsers.php"
    }
  ]
}
---

# Only a User with a verified email publishes, comments, likes, bookmarks, reposts or votes

Until their email is verified, a User who tries to publish, comment, like, bookmark, repost or vote is sent to verify it, and profiles and post pages send them there too.
