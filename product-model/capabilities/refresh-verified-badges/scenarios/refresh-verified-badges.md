---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The daily check reaches a User with a verified badge",
      "kind": "condition",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "GitHub username",
            "Verified"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      },
      "unattended": true
    },
    {
      "text": "The Product asks GitHub about the sponsorship and updates the badges",
      "kind": "product",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Verified",
            "Company verified"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    }
  ]
}
---

# Refresh a verified User's badge

## Trigger

The daily check reaches a verified User.

## Outcome

The User keeps the badge while sponsoring and loses it when the sponsorship ended.
