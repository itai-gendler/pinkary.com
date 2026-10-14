---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User writes a reply of up to 1000 characters under a post and sends it",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Content"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::post"
        }
      }
    },
    {
      "text": "The Product publishes the comment and notifies the post's author and the mentioned Users",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "comment",
          "effect": "creates",
          "to": "Published",
          "facts": [
            "Content",
            "Images",
            "Published at"
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
        },
        {
          "entity": "post",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::post"
        }
      }
    }
  ]
}
---

# Comment on a post

## Trigger

A User wants to reply to a post.

## Outcome

The comment shows under the post, whose author is notified unless it is the commenter.
