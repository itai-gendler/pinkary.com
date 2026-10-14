---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "vote",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "casts",
          "entity": "user"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Actions/Questions/UpdatePollVote.php"
    }
  ]
}
---

# Only the voter takes back their vote

Choosing the voted option again removes the vote.
