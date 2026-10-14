---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest enters a name, username, email and password, accepts the terms and solves the challenge",
      "kind": "actor",
      "actor": "guest",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::register"
        }
      }
    },
    {
      "text": "The Product creates the User with an avatar fetched from GitHub or Gravatar and signs the Guest in",
      "kind": "product",
      "actor": "guest",
      "entities": [
        {
          "entity": "user",
          "effect": "creates",
          "facts": [
            "Name",
            "Username",
            "Email",
            "Password",
            "Avatar",
            "Mail preference",
            "Default feed",
            "Who can ask questions",
            "Ask anonymously by default"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::register"
        }
      }
    },
    {
      "text": "The Product emails a verification message to the address",
      "kind": "product",
      "actor": "guest",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Email",
            "Name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::register"
        }
      }
    }
  ]
}
---

# Register a new account

## Trigger

A Guest wants a profile of their own.

## Outcome

The Guest is signed in to a new User whose email is not yet verified, a verification email is on its way, and the Product asks them to verify their email before using their profile.

## Edge cases

- The challenge is only asked for where the Product runs publicly.
