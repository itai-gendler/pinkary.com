---
{
  "relations": [
    {
      "entity": "post",
      "verb": "holds",
      "cardinality": "one-to-many"
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
      "target": "app/Livewire/Concerns/HasChannelPicker.php"
    }
  ]
}
---

# Channel

A topic posts are shared in, with a page of its own.

## Information kept

- **Name** — the channel name, 2 to 50 letters, digits, spaces, dashes or underscores
- **Address** — the unique name in the channel's web address, derived from its name
- **Post count** — how many posts were shared in the channel
