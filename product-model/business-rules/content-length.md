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
    },
    {
      "type": "capability",
      "id": "answer-question"
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
      "target": "app/Rules/NoBlankCharacters.php"
    }
  ]
}
---

# A question holds up to 255 characters, and a post, answer or comment up to 1000

Text made only of blank characters is refused. A thread holds up to ten posts.
