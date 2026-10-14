---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens the followers of a profile",
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

# A User lists followers

## Trigger

A User looks at who follows a profile.

## Outcome

The User sees the followers and which of them they follow or are followed by.
