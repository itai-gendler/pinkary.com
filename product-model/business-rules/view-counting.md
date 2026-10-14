---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "post",
      "effect": "changes",
      "facts": [
        "Views"
      ]
    },
    {
      "type": "entity",
      "id": "user",
      "effect": "changes",
      "facts": [
        "Profile views"
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "guest",
        "user"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Jobs/IncrementViews.php"
    }
  ]
}
---

# Anyone's view is counted once per viewer every two hours, and never for bots

Profile views and the views of posts and answers count signed-in Users by account and Guests by browser session.
