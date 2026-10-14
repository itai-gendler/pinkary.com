---
{
  "kind": "edge",
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
      "text": "The credentials match a User with two-factor authentication confirmed",
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
      "text": "The Product asks for the authenticator code",
      "kind": "product",
      "actor": "guest",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::two-factor-challenge"
        }
      }
    }
  ]
}
---

# Log in when two-factor authentication is on

## Trigger

A Guest whose User has two-factor authentication logs in.

## Outcome

The password is accepted and the Guest is taken to the two-factor challenge to finish logging in.
