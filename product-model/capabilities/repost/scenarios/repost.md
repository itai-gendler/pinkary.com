---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User reposts a post",
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
      "text": "The Product records the repost and notifies the post's author",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "repost",
          "effect": "creates",
          "facts": [
            "Reposted at"
          ]
        },
        {
          "entity": "notification",
          "effect": "creates",
          "facts": [
            "Kind",
            "Subject",
            "Received at"
          ]
        },
        {
          "entity": "post",
          "effect": "reads",
          "facts": []
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

# Repost a post

## Trigger

A User wants their followers to see someone's post.

## Outcome

The post appears again at the top of Recent, in the User's followers' Following feed and on the User's profile, marked as reposted by them; its author is notified.

## Edge cases

- Reposting one's own post notifies nobody.
- Reposting something already reposted changes nothing.
