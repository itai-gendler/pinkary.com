---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "follow",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "actors": [
        "user"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Policies/UserPolicy.php#follow"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Actions/Users/CreateFollow.php"
    }
  ]
}
---

# A User follows other Users, never themselves

Following requires being signed in; following someone already followed changes nothing.
