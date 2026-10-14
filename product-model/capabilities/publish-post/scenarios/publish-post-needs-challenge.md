---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User sends an update without solving the challenge",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::home"
        }
      }
    },
    {
      "text": "Nobody follows the User",
      "kind": "condition",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "follow",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::home"
        }
      }
    },
    {
      "text": "The Product refuses the post and asks for the challenge",
      "kind": "product",
      "actor": "user",
      "entities": [
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

# A User without followers skips the challenge

## Trigger

A User nobody follows sends a post without solving the challenge.

## Outcome

The post is not published until the challenge is solved.
