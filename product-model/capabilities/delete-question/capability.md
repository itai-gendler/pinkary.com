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
      "target": "resources/views/livewire/questions/show.blade.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Observers/QuestionObserver.php#deleted"
    }
  ]
}
---

# Delete question

The recipient deletes an answered question from their profile.
