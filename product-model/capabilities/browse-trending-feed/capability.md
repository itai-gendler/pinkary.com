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
      "target": "app/Queries/Feeds/TrendingQuestionsFeed.php"
    }
  ]
}
---

# Browse trending feed

Anyone reads Trending: answers and posts of the last seven days ranked by likes and comments and by how recent they are.
