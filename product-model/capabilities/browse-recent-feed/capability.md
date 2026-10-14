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
  "domain": "feed",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Queries/Feeds/RecentQuestionsFeed.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Http/Responses/HomeFeedResponse.php"
    }
  ]
}
---

# Browse recent feed

Anyone reads Recent: the latest answers, posts and reposts across Pinkary, one entry per thread with its context.
