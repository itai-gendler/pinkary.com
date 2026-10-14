---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens Home",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Content",
            "Images",
            "Published at",
            "Poll options",
            "Poll results",
            "Channel",
            "Views"
          ]
        },
        {
          "entity": "question",
          "effect": "reads",
          "facts": [
            "Question text",
            "Anonymous",
            "Answer",
            "Answered at",
            "Views"
          ]
        },
        {
          "entity": "repost",
          "effect": "reads",
          "facts": [
            "Reposted at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::home"
        }
      }
    }
  ]
}
---

# A User reads Recent

## Trigger

A User whose default feed is Recent opens Home.

## Outcome

The User sees the newest activity with their own likes, bookmarks, reposts and votes marked.
