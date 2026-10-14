---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User drags a link to another position",
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
      "text": "The Product saves the order of the User's own links",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Link order"
          ]
        },
        {
          "entity": "link",
          "effect": "reads",
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

# Reorder links

## Trigger

A User wants a link higher up.

## Outcome

The profile lists the links in the new order; links never ordered come last.
