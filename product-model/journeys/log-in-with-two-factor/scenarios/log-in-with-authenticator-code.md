---
{
  "kind": "primary",
  "result": "achieved",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest enters their email and password",
      "kind": "actor",
      "actor": "guest",
      "entities": [],
      "capability": "log-in",
      "contexts": {
        "web": {
          "place": "web::public::log-in"
        }
      }
    },
    {
      "text": "The Product asks for the authenticator code",
      "kind": "product",
      "actor": "guest",
      "entities": [],
      "capability": "log-in",
      "contexts": {
        "web": {
          "place": "web::public::two-factor-challenge"
        }
      }
    },
    {
      "text": "The Guest enters the code from their authenticator app",
      "kind": "actor",
      "actor": "guest",
      "entities": [],
      "capability": "complete-two-factor-challenge",
      "contexts": {
        "web": {
          "place": "web::public::two-factor-challenge"
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
      "capability": "complete-two-factor-challenge",
      "contexts": {
        "web": {
          "place": "web::public::two-factor-challenge"
        }
      }
    }
  ]
}
---

# Log in with password and authenticator code

## Trigger

A Guest with two-factor authentication logs in.

## Outcome

The Guest is signed in.
