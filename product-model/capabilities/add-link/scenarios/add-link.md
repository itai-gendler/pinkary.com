---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User enters a description and an address to add",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    },
    {
      "text": "The Product adds https:// when missing and creates the link",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "link",
          "effect": "creates",
          "to": "Visible",
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

# Add a link

## Trigger

A User wants to share another page.

## Outcome

The link is visible at the end of the profile's links.
