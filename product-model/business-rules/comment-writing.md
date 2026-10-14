---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "comment",
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
      "target": "app/Livewire/Questions/Create.php"
    }
  ]
}
---

# Only a User with a verified email comments

Comments are open to every signed-in User whose email is verified, on any post, answered question or comment they can see.
