---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "pin-to-profile"
    },
    {
      "type": "capability",
      "id": "unpin-from-profile"
    },
    {
      "type": "capability",
      "id": "view-profile"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Actions/Questions/UpdateQuestionPin.php"
    }
  ]
}
---

# A profile has at most one pinned post or answered question

Pinning something unpins whatever was pinned before; the pinned item is shown first on the profile.
