---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "channel"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Models/Channel.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Actions/Questions/CreateThread.php"
    }
  ]
}
---

# Announcements is reserved for Pinkary's administrators

A channel named Announcements is neither offered to nor created by other Users; a post sent with it is published without a channel.
