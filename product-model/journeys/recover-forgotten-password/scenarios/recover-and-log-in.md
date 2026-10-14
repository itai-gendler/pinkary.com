---
{
  "kind": "primary",
  "result": "achieved",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest uses the reset email and enters a new password twice",
      "kind": "actor",
      "actor": "guest",
      "entities": [],
      "capability": "reset-password",
      "contexts": {
        "web": {
          "place": "web::public::reset-password"
        }
      }
    },
    {
      "text": "The Product saves the new password and takes the Guest to log in",
      "kind": "product",
      "actor": "guest",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Password"
          ]
        }
      ],
      "capability": "reset-password",
      "contexts": {
        "web": {
          "place": "web::public::reset-password"
        }
      }
    },
    {
      "text": "The Guest enters their email and new password",
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
      "capability": "log-in",
      "contexts": {
        "web": {
          "place": "web::public::log-in"
        }
      }
    }
  ]
}
---

# Reset the password and log in

## Trigger

A Guest cannot remember their password.

## Outcome

The Guest is signed in with the new password.
