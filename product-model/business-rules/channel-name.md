---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "publish-post"
    },
    {
      "type": "capability",
      "id": "edit-post"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Livewire/Concerns/HasChannelPicker.php"
    }
  ]
}
---

# A channel name has 2 to 50 letters, digits, spaces, dashes or underscores, and one name makes one channel

Two names with the same address lead to the same channel; picking a name that exists joins it.
