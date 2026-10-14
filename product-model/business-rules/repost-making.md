---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "repost",
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
      "target": "app/Policies/QuestionPolicy.php#repost"
    }
  ]
}
---

# Only a User with a verified email reposts, and only what is answered and visible

Unanswered, ignored, reported or deleted things cannot be reposted; each User reposts a thing at most once.
