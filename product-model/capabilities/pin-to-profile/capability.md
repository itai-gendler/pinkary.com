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
      "target": "app/Actions/Questions/UpdateQuestionPin.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Policies/QuestionPolicy.php#pin"
    }
  ]
}
---

# Pin to profile

A User pins one of their posts or answered questions to the top of their profile; it replaces any pinned one.
