---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "profile",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Livewire/Questions/Create.php#Create"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Policies/UserPolicy.php#askQuestion"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Observers/QuestionObserver.php"
    }
  ]
}
---

# Ask question

A User asks another User a question on their profile, anonymously or not.
