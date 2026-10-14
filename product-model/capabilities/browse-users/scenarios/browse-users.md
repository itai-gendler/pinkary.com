---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest opens Users",
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
            "Verified"
          ]
        },
        {
          "entity": "link",
          "effect": "reads",
          "facts": [
            "URL"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::users"
        }
      }
    }
  ]
}
---

# A Guest browses Users

## Trigger

A Guest looks for interesting people.

## Outcome

The Guest sees a shuffled selection of verified and popular Users with their links.
