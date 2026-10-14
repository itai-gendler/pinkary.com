---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "link",
      "effect": "changes",
      "facts": [
        "Description",
        "URL"
      ]
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

# Only the owner edits a link

A link's description and address change only through the User whose profile it is on.
