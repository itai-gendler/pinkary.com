---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "publish-post"
    },
    {
      "type": "capability",
      "id": "vote-in-poll"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Actions/Questions/CreateThread.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Livewire/Questions/PollVoting.php"
    }
  ]
}
---

# A poll has 2 to 4 options of up to 40 characters and stays open 1 to 7 days

Posts and comments can be polls; questions cannot. Once the poll ends, votes are refused.
