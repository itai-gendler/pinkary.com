---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses to log out of another account in the switcher and confirms",
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
      "text": "The Product removes that account from the switcher",
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

# Log out of another added account

## Trigger

A User no longer wants an account listed in the switcher.

## Outcome

The account leaves the switcher; the current account stays signed in.
