---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "link",
      "effect": "changes",
      "facts": [
        "Clicks"
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "guest",
        "user"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Actions/Links/UpdateLinkClicks.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Actions/Links/UpdateLink.php"
    }
  ]
}
---

# A link counts each visitor's click at most once a day and never the owner's

Changing a link's address starts its count from zero.
