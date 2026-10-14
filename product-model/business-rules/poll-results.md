---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "post",
      "effect": "changes",
      "facts": [
        "Poll results"
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "user"
      ],
      "when": [
        {
          "entity": "user",
          "fact": "Email verified at",
          "present": true
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

# A poll's results change only through votes

Each vote, change of vote or withdrawal moves the counts of the options it concerns.
