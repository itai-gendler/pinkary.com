---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "edit-answer"
    },
    {
      "type": "capability",
      "id": "edit-post"
    },
    {
      "type": "capability",
      "id": "edit-comment"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Livewire/Questions/Edit.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Actions/Questions/UpdateQuestion.php"
    }
  ]
}
---

# Answers, posts and comments are editable for 24 hours, and an edit clears their likes

After 24 hours from answering or publishing, the text can no longer be changed. Saving a changed text removes the likes it had.
