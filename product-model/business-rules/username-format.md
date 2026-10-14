---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "register-account"
    },
    {
      "type": "capability",
      "id": "edit-profile"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Rules/Username.php"
    }
  ]
}
---

# A username is 4 to 50 letters, digits or underscores, holds two letters and is neither reserved nor taken

Usernames are unique ignoring letter case, must contain at least two letters, and may not be one of the reserved words that name Pinkary's own pages and common services.
