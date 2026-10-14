---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "ask-question"
    },
    {
      "type": "capability",
      "id": "publish-post"
    },
    {
      "type": "capability",
      "id": "add-comment"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Livewire/Questions/Create.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Actions/Questions/EnsureCanPublish.php"
    }
  ]
}
---

# A User sends at most 3 questions, posts or comments a minute and 30 a day

Every post of a thread counts toward the daily limit.
