---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "link",
      "effect": "changes",
      "to": "Hidden"
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

# Only the owner hides a link

Hidden links stay visible to their owner only.
