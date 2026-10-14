---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest opens the following list of a profile",
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

# A Guest lists who a User follows

## Trigger

A Guest wants to see whom someone follows.

## Outcome

The Guest sees the followed people.
