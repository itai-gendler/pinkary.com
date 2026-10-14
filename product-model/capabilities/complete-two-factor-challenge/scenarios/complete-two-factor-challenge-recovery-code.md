---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest enters one of their recovery codes",
      "kind": "actor",
      "actor": "guest",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::two-factor-challenge"
        }
      }
    },
    {
      "text": "The Product signs the Guest in, uses up the recovery code and adds the account to the switcher",
      "kind": "product",
      "actor": "guest",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Recovery codes"
          ]
        },
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
          "place": "web::public::two-factor-challenge"
        }
      }
    }
  ]
}
---

# Use a recovery code

## Trigger

A Guest without their authenticator app finishes logging in.

## Outcome

The Guest is signed in and the used recovery code no longer works.
