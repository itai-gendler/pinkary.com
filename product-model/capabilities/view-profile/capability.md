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
  "domain": "profile",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Http/Controllers/UserController.php#UserController"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Livewire/Links/Index.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Queries/Feeds/UserQuestionsFeed.php"
    }
  ]
}
---

# View profile

Anyone opens a User's profile at /@username: avatar, name, badges, bio, follower and post counts, views, visible links and the answers and posts, with the pinned one first.
