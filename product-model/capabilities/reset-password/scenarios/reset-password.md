---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest enters their email",
      "kind": "actor",
      "actor": "guest",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::forgot-password"
        }
      }
    },
    {
      "text": "The Product emails a password reset message",
      "kind": "product",
      "actor": "guest",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Email"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::forgot-password"
        }
      }
    },
    {
      "text": "The Guest uses the reset email and enters a new password twice",
      "kind": "actor",
      "actor": "guest",
      "entities": [],
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
      "contexts": {
        "web": {
          "place": "web::public::reset-password"
        }
      }
    }
  ]
}
---

# Reset a forgotten password

## Trigger

A Guest cannot remember their password.

## Outcome

The password is changed, other remembered sessions stop working, and the Guest is taken to log in.
