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
      "target": "app/Actions/Questions/CreateRepost.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Observers/RepostObserver.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Policies/QuestionPolicy.php#repost"
    }
  ]
}
---

# Repost

A User reposts a post, an answered question or a comment so it shows in their followers' feeds and on their profile.
