---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User shows a hidden link",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "link",
          "effect": "reads",
          "facts": [
            "Description"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    },
    {
      "text": "The Product shows the link",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "link",
          "effect": "changes",
          "from": "Hidden",
          "to": "Visible",
          "facts": []
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

# Show a hidden link

## Trigger

A User wants a hidden link back on the profile.

## Outcome

Everyone sees the link again.
