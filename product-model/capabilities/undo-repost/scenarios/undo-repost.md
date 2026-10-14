---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User undoes their repost of a post",
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
    },
    {
      "text": "The Product removes the repost and its notification",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "repost",
          "effect": "removes"
        },
        {
          "entity": "notification",
          "effect": "removes"
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

# Undo a repost

## Trigger

A User no longer wants to share a post.

## Outcome

The repost leaves the feeds and the profile, and its notification is withdrawn.
