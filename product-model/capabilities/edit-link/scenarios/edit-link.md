---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User edits a link's description and address and saves",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "link",
          "effect": "reads",
          "facts": [
            "Description",
            "URL"
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
      "text": "The Product saves the link and resets its clicks when the address changed",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "link",
          "effect": "changes",
          "facts": [
            "Description",
            "URL",
            "Clicks"
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

# Edit a link

## Trigger

A User's link moved or needs a better label.

## Outcome

The link shows the new description and address; a new address starts its click count again.
