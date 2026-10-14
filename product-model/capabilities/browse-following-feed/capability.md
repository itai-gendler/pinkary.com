---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "feed",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Queries/Feeds/QuestionsFollowingFeed.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "resources/views/home/following.blade.php"
    }
  ]
}
---

# Browse following feed

A User reads Following: answers, posts and reposts from the people they follow and from themselves.
