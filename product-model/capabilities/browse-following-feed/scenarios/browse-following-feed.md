---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens Following",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "follow",
          "effect": "reads",
          "facts": []
        },
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

# Read Following

## Trigger

A User wants news from the people they follow.

## Outcome

The User sees their followed people's latest activity, newest first.
