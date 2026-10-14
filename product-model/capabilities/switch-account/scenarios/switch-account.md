---
{
  "kind": "primary",
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
      "text": "The Product signs in to that account",
      "kind": "product",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in"
        }
      }
    }
  ]
}
---

# Switch to another added account

## Trigger

A User wants to act as another of their accounts.

## Outcome

The browser is signed in to the chosen account, on the page the User was on.
