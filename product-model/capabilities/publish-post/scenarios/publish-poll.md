---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User writes an update, turns it into a poll with 2 to 4 options and picks 1 to 7 days",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::home"
        }
      }
    },
    {
      "text": "The Product publishes the post with its poll",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "effect": "creates",
          "to": "Published",
          "facts": [
            "Content",
            "Published at",
            "Poll options",
            "Poll ends",
            "Poll results"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::home"
        }
      }
    }
  ]
}
---

# Publish a poll

## Trigger

A User wants the community's opinion.

## Outcome

The post carries a poll open for the chosen days.
