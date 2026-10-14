---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User picks another account in the switcher",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "switcher-entry",
          "effect": "reads",
          "facts": [
            "Username"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in"
        }
      }
    },
    {
      "text": "That account logged out elsewhere, changed its password or was deleted",
      "kind": "condition",
      "actor": "user",
      "entities": [
        {
          "entity": "switcher-entry",
          "effect": "reads",
          "facts": [
            "Username"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in"
        }
      }
    },
    {
      "text": "The Product drops it from the switcher and refuses the switch",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "switcher-entry",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in"
        }
      }
    }
  ]
}
---

# Switch to an account that is no longer valid

## Trigger

An added account logged out elsewhere, changed its password or was deleted.

## Outcome

The account disappears from the switcher and nothing is switched.
