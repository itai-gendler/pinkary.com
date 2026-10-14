---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "question"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "resources/views/livewire/questions/show.blade.php"
    }
  ]
}
---

# An anonymous question never shows who asked it

When a question is anonymous, its asker is hidden on the profile, the question page, the feeds and the recipient's notifications. Questions start anonymous or not according to the asker's default.
