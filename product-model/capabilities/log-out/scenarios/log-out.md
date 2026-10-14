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
      "text": "The Product removes the account from the switcher and ends the session",
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

# Log out of the only account

## Trigger

A User is done with Pinkary on this browser.

## Outcome

The User is signed out and the switcher is empty.
