---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens the likes of their own post",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Content"
          ]
        },
        {
          "entity": "like",
          "effect": "reads",
          "facts": [
            "Liked at"
          ]
        },
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Name",
            "Username",
            "Avatar"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::post"
        }
      }
    }
  ]
}
---

# See who liked a post

## Trigger

A User wonders who liked their post.

## Outcome

The User sees the likers, most recent first, and can follow them.
