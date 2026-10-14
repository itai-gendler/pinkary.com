---
{
  "entities": [
    {
      "entity": "comment",
      "shows": [
        "Content",
        "Images",
        "Poll options",
        "Poll results",
        "Published at"
      ]
    },
    {
      "entity": "post",
      "shows": [
        "Channel",
        "Content",
        "Images",
        "Poll options",
        "Poll results",
        "Published at",
        "Views"
      ]
    },
    {
      "entity": "question",
      "shows": [
        "Anonymous",
        "Answer",
        "Answered at",
        "Question text",
        "Views"
      ]
    },
    {
      "entity": "user",
      "shows": [
        "Avatar",
        "Name",
        "Username"
      ]
    }
  ],
  "entryPoints": [
    {
      "web": "/@{username}/questions/{id}"
    }
  ]
}
---

# Post

One post or answered question with its thread and comments.
