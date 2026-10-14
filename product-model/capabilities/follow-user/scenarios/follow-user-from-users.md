---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses Follow beside a User in the list",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Name",
            "Username"
          ]
        },
        {
          "entity": "follow",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::users"
        }
      }
    },
    {
      "text": "The Product records the follow and notifies the followed User",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "follow",
          "effect": "creates",
          "to": "Following",
          "facts": []
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
          "place": "web::signed-in::users"
        }
      }
    }
  ]
}
---

# Follow from the Users page

## Trigger

A User finds someone on the Users page.

## Outcome

The User follows them and the followed User is notified.

## Edge cases

- Following someone already followed changes nothing and notifies nobody.
