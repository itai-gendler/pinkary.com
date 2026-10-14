---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses to add an existing account and enters its email and password",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::log-in"
        }
      }
    },
    {
      "text": "The Product signs in to that account and adds it to the switcher",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "switcher-entry",
          "effect": "creates",
          "facts": [
            "Username"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::log-in"
        }
      }
    }
  ]
}
---

# Add an existing account

## Trigger

A signed-in User wants to use a second account in the same browser.

## Outcome

The User is signed in to the other account and both accounts are in the switcher.
