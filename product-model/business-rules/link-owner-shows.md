---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "link",
      "effect": "changes",
      "to": "Visible"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "has",
          "entity": "user"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Policies/LinkPolicy.php"
    }
  ]
}
---

# Only the owner shows a hidden link

A hidden link returns to the profile only through its owner.
