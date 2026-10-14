---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "vote",
      "effect": "changes"
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

# Only the voter changes their vote

Choosing another option moves the vote.
