---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens Following",
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
      "text": "Nobody the User follows has published anything",
      "kind": "condition",
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

# Nobody followed yet

## Trigger

A User who follows nobody opens Following.

## Outcome

The User is told the feed is empty and invited to follow more people.
