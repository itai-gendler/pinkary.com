---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest enters a wrong code",
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
      "text": "The Product refuses the code",
      "kind": "condition",
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

# Enter a wrong code

## Trigger

A Guest enters a code that does not match.

## Outcome

The Guest stays signed out; after five attempts a minute they must wait.
