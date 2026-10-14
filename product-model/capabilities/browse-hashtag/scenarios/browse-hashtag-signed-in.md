---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens a hashtag",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "hashtag",
          "effect": "reads",
          "facts": [
            "Name"
          ]
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
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::hashtag"
        }
      }
    }
  ]
}
---

# A User opens a hashtag

## Trigger

A User follows a #tag.

## Outcome

The User sees everything carrying the tag, newest first.
