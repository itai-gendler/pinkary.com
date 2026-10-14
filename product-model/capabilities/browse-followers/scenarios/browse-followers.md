---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest opens the followers of a profile",
      "kind": "actor",
      "actor": "guest",
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
          "place": "web::public::profile"
        }
      }
    }
  ]
}
---

# A Guest lists a User's followers

## Trigger

A Guest wonders who follows someone.

## Outcome

The Guest sees the followers, newest first.
