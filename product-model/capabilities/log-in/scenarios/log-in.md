---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest enters their email and password",
      "kind": "actor",
      "actor": "guest",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::log-in"
        }
      }
    },
    {
      "text": "The credentials match a User without two-factor authentication",
      "kind": "condition",
      "actor": "guest",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Two-factor authentication"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::log-in"
        }
      }
    },
    {
      "text": "The Product signs the Guest in and adds the account to the switcher",
      "kind": "product",
      "actor": "guest",
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
          "place": "web::public::log-in"
        }
      }
    }
  ]
}
---

# Log in with email and password

## Trigger

A Guest with an account wants to sign in.

## Outcome

The Guest is signed in as their User, the account is added to this browser's switcher, and they land where they were going or on Home.
