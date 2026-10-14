---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "browse-recent-feed"
    },
    {
      "type": "capability",
      "id": "browse-following-feed"
    },
    {
      "type": "capability",
      "id": "view-profile"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Queries/Feeds/RecentQuestionsFeed.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Queries/Feeds/FeedThread.php"
    }
  ]
}
---

# Feeds show each thread once, at its latest activity

Recent, Following and profiles show the latest post of each thread with the posts it continues, and reposts at the time they were made.
