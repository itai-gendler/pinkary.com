---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "link",
      "effect": "removes"
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

# Only the owner deletes a link

Deleting a link is the owner's alone.
