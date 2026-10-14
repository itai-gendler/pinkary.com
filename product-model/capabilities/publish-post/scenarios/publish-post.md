---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User writes an update of up to 1000 characters, adds up to three images and sends it",
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
      "text": "The Product publishes the post, records its hashtags and notifies the mentioned Users",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "effect": "creates",
          "to": "Published",
          "facts": [
            "Content",
            "Images",
            "Published at"
          ]
        },
        {
          "entity": "hashtag",
          "effect": "creates",
          "facts": [
            "Name"
          ]
        },
        {
          "entity": "notification",
          "effect": "creates",
          "facts": [
            "Kind",
            "Subject",
            "Received at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::home"
        }
      }
    },
    {
      "text": "The Product confirms with a way to view the update",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": []
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

# Publish a post

## Trigger

A User has something to share.

## Outcome

The post is on the User's profile and at the top of Recent; mentioned Users are notified and its hashtags are recorded.

## Edge cases

- Images uploaded while writing and then removed from the text are discarded.
