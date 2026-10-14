---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest opens a User's profile",
      "kind": "actor",
      "actor": "guest",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Name",
            "Username",
            "Avatar",
            "Bio",
            "Verified",
            "Company verified",
            "Profile views",
            "Link shape",
            "Link color"
          ]
        },
        {
          "entity": "link",
          "effect": "reads",
          "facts": [
            "Description",
            "URL"
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
            "Views",
            "Pinned"
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
            "Views",
            "Pinned"
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
          "place": "web::public::profile"
        }
      }
    },
    {
      "text": "The Product counts the view once for this visitor in two hours, ignoring bots",
      "kind": "product",
      "actor": "guest",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Profile views"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::profile"
        }
      }
    }
  ]
}
---

# A Guest views a profile

## Trigger

A Guest opens someone's Pinkary link.

## Outcome

The Guest sees the profile, its visible links and its answered questions, posts and reposts, and the profile view is counted.
