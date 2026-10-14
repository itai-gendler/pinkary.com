---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "question",
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
      "target": "app/Policies/UserPolicy.php#askQuestion"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Enums/UserQuestionPreference.php"
    }
  ]
}
---

# A question is asked only by a User with a verified email whom the recipient accepts questions from

Each User chooses who can ask them questions: Everyone, Following (only people they follow) or No one. A question refused by that choice is never sent.
