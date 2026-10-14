---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User writes a first update and up to nine more, each optionally a poll",
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
      "text": "The Product publishes the posts in order, each continuing the one before",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "as": "first-post",
          "effect": "creates",
          "to": "Published",
          "facts": [
            "Content",
            "Published at"
          ]
        },
        {
          "entity": "post",
          "as": "next-post",
          "effect": "creates",
          "to": "Published",
          "facts": [
            "Content",
            "Published at",
            "Thread"
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

# Publish a thread

## Trigger

A User has more to say than one post holds.

## Outcome

The posts are published together as one thread, the first carrying any channel.

## Edge cases

- Each post of a thread counts toward the daily limit.
