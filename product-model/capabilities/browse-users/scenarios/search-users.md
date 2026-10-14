---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User types part of a name or username",
      "kind": "actor",
      "actor": "user",
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
          "entity": "follow",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::users"
        }
      }
    }
  ]
}
---

# A User searches people

## Trigger

A User looks for someone they know.

## Outcome

The User sees up to ten matching Users, those with the most answers first, and whether they follow each other.
