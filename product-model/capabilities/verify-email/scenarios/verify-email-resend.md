---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User asks the Product to send the verification email again",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::verify-email"
        }
      }
    },
    {
      "text": "The Product emails a new verification message",
      "kind": "product",
      "actor": "user",
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
          "place": "web::signed-in::verify-email"
        }
      }
    }
  ]
}
---

# Ask for a new verification link

## Trigger

A User did not get or lost the verification email.

## Outcome

A new verification email is sent and the User still has to follow it.
