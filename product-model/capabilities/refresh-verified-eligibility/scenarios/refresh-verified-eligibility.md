---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses Refresh Verified Eligibility",
      "kind": "actor",
      "actor": "user",
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
          "place": "web::signed-in::settings"
        }
      }
    },
    {
      "text": "The Product asks GitHub about the sponsorship and updates the badges",
      "kind": "product",
      "actor": "user",
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
          "place": "web::signed-in::settings"
        }
      }
    }
  ]
}
---

# Refresh verified eligibility

## Trigger

A User sponsored Pinkary after connecting GitHub.

## Outcome

The badges match the current sponsorship and the User is told whether they are verified.
