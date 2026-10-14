---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest enters the code from their authenticator app",
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
          "place": "web::public::two-factor-challenge"
        }
      }
    }
  ]
}
---

# Enter the authenticator code

## Trigger

The Product asks a Guest for their two-factor code.

## Outcome

The Guest is signed in and the account is added to the switcher.
