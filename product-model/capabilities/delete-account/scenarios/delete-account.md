---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses Delete Account and enters their password",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::settings"
        }
      }
    },
    {
      "text": "The Product signs the User out and deletes the User with everything they own",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "removes"
        },
        {
          "entity": "link",
          "effect": "removes",
          "from": "Visible",
          "with": "user"
        },
        {
          "entity": "follow",
          "effect": "removes",
          "from": "Following",
          "with": "user"
        },
        {
          "entity": "notification",
          "effect": "removes",
          "with": "user"
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

# Delete the account

## Trigger

A User leaves Pinkary.

## Outcome

The User, their links, questions, posts, comments, reposts, follows and notifications are gone and the person is signed out on Home.
