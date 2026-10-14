---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "follow",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "starts",
          "entity": "user"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Policies/UserPolicy.php#unfollow"
    }
  ]
}
---

# Only the follower ends a follow

A follow also ends when either User deletes their account.
