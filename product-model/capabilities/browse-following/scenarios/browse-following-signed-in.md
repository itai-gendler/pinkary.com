---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens the following list of a profile",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "follow",
          "effect": "reads",
          "facts": []
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
          "place": "web::signed-in::profile"
        }
      }
    }
  ]
}
---

# A User lists who someone follows

## Trigger

A User looks for people to follow.

## Outcome

The User sees the followed people and can follow them too.
