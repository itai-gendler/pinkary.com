---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest opens Home",
      "kind": "actor",
      "actor": "guest",
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
          "entity": "comment",
          "effect": "reads",
          "facts": [
            "Content",
            "Published at"
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
          "place": "web::public::home"
        }
      }
    },
    {
      "text": "The Product counts the views of the posts the Guest scrolls past",
      "kind": "product",
      "actor": "guest",
      "entities": [
        {
          "entity": "post",
          "effect": "changes",
          "facts": [
            "Views"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::home"
        }
      }
    }
  ]
}
---

# A Guest reads Recent

## Trigger

A Guest opens Pinkary.

## Outcome

The Guest sees the newest activity first, with the latest post of each thread and the posts it replies to.
