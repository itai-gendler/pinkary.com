---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "repost",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "makes",
          "entity": "user"
        }
      ]
    },
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
      "target": "app/Policies/RepostPolicy.php"
    }
  ]
}
---

# Only the User who reposted undoes the repost

A repost also goes when its post, answer or comment is deleted.
