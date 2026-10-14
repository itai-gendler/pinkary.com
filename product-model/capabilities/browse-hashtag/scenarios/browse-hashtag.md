---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest opens a hashtag",
      "kind": "actor",
      "actor": "guest",
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
          "place": "web::public::hashtag"
        }
      }
    }
  ]
}
---

# A Guest opens a hashtag

## Trigger

A Guest follows a #tag in a post.

## Outcome

The Guest sees everything carrying the tag, ignoring letter case, newest first.
