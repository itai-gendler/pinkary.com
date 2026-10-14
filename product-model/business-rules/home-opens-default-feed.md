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
      "id": "browse-trending-feed"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Http/Responses/HomeFeedResponse.php"
    }
  ]
}
---

# Home opens the User's default feed

A signed-in User who opens Pinkary lands on Recent, Following or Trending as their default feed says; Guests land on Recent.
