---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "vote",
      "effect": "creates"
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

# Only a User with a verified email votes, once per poll

A User holds one vote per poll and may move or withdraw it while the poll is open.
