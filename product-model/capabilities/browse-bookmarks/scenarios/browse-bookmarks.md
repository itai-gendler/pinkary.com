---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens Bookmarks",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "bookmark",
          "effect": "reads",
          "facts": [
            "Bookmarked at"
          ]
        },
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Content",
            "Images",
            "Published at"
          ]
        },
        {
          "entity": "question",
          "effect": "reads",
          "facts": [
            "Question text",
            "Answer"
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
          "place": "web::signed-in::bookmarks"
        }
      }
    }
  ]
}
---

# Browse bookmarks

## Trigger

A User wants what they saved.

## Outcome

The User sees their bookmarked posts, answers and comments, most recently saved first.
