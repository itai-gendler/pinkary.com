---
{
  "availability": [
    {
      "place": "web::public"
    },
    {
      "place": "web::signed-in"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Http/Controllers/HashtagController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Queries/Feeds/RecentQuestionsFeed.php"
    }
  ]
}
---

# Browse hashtag

Anyone opens a hashtag and reads the answers, posts and comments carrying it, newest first.
