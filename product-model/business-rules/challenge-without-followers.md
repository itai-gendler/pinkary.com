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
      "target": "app/Livewire/Questions/Create.php#needsCaptcha"
    }
  ]
}
---

# A User nobody follows solves a challenge to send a question, post or comment

Where the Product runs publicly, the composer asks a User with no followers for a challenge before sending.
