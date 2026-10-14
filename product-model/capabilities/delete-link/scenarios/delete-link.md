---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses to delete a link and confirms",
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
      "text": "The Product deletes the link",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "link",
          "effect": "removes",
          "from": "Visible"
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

# Delete a link

## Trigger

A User no longer wants a link.

## Outcome

The link is gone, and a fetched avatar is fetched again.

## Edge cases

- A hidden link is deleted the same way.
