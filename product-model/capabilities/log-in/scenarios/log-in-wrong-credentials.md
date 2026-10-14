---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest enters an email and password that do not match",
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
      "text": "The Product refuses the log in and keeps the form",
      "kind": "condition",
      "actor": "guest",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::log-in"
        }
      }
    }
  ]
}
---

# Log in with wrong credentials

## Trigger

A Guest mistypes their email or password.

## Outcome

The Guest stays signed out; after five attempts a minute they must wait.
