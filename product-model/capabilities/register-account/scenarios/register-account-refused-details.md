---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest enters a username that is taken, reserved or not letters, digits and underscores, or an email that is an alias, from a refused provider or blocked",
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
      "text": "The Product refuses the details and keeps the form",
      "kind": "condition",
      "actor": "guest",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::register"
        }
      }
    }
  ]
}
---

# Registration refused for its details

## Trigger

A Guest registers with a username or email the Product does not accept.

## Outcome

No account is created and the Guest sees which detail to change.
