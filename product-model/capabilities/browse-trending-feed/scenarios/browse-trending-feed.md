---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest opens Trending",
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
            "Content"
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

# A Guest reads Trending

## Trigger

A Guest wants what is popular.

## Outcome

The Guest sees the week's most engaging answers and posts first.
