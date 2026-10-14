---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens one of their own links",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "link",
          "effect": "reads",
          "facts": [
            "Description",
            "URL"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    },
    {
      "text": "The link belongs to the User, so the click is not counted",
      "kind": "condition",
      "actor": "user",
      "entities": [
        {
          "entity": "link",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "user",
          "effect": "reads",
          "facts": []
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

# The owner opens their own link

## Trigger

A User opens a link on their own profile.

## Outcome

The link opens and the click is not counted.
