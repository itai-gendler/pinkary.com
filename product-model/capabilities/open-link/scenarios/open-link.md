---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Guest opens a link on a profile",
      "kind": "actor",
      "actor": "guest",
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
          "place": "web::public::profile"
        }
      }
    },
    {
      "text": "The Product counts the click once a day per visitor",
      "kind": "product",
      "actor": "guest",
      "entities": [
        {
          "entity": "link",
          "effect": "changes",
          "facts": [
            "Clicks"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::profile"
        }
      }
    }
  ]
}
---

# A Guest opens a link

## Trigger

A Guest wants what a profile links to.

## Outcome

The link opens and its click count grows by one, at most once a day for this visitor.
