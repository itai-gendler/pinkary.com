---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses Unfollow on a profile they follow",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Name",
            "Username"
          ]
        },
        {
          "entity": "follow",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    },
    {
      "text": "The Product removes the follow and the new-follower notification",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "follow",
          "effect": "removes",
          "from": "Following"
        },
        {
          "entity": "notification",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    }
  ]
}
---

# Unfollow a User

## Trigger

A User no longer wants someone's posts in Following.

## Outcome

The follow is gone and the followed User's new-follower notification is withdrawn.
