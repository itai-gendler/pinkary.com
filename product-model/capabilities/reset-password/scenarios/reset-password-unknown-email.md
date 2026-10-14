---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest enters an email",
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
      "text": "No User has that email",
      "kind": "condition",
      "actor": "guest",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::forgot-password"
        }
      }
    }
  ]
}
---

# Ask a reset for an unknown email

## Trigger

A Guest enters an email no User has.

## Outcome

No email is sent and the Guest is told the address is unknown.
