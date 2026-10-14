---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User logs out",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in"
        }
      }
    },
    {
      "text": "The Product removes the current account from the switcher",
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
    },
    {
      "text": "The Product signs in to the most recently added remaining account",
      "kind": "product",
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
    }
  ]
}
---

# Log out while other accounts are added

## Trigger

A User with several added accounts logs out of the current one.

## Outcome

The current account leaves the switcher and the browser is signed in to another added account.
