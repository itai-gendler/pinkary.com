---
{
  "relations": [
    {
      "entity": "comment",
      "verb": "receives",
      "cardinality": "one-to-many"
    },
    {
      "entity": "like",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "bookmark",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "repost",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "vote",
      "verb": "has",
      "cardinality": "one-to-many"
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
      "target": "app/Livewire/Questions/Create.php"
    }
  ]
}
---

# Post

An update a User shares on their own profile and in the feeds, alone or as one post of a thread.

## Information kept

- **Content** — the text, up to 1000 characters, with links, mentions, hashtags and code
- **Images** — up to three images placed in the content
- **Published at** — when the post was shared
- **Edited at** — when the post was last edited
- **Poll options** — two to four options of up to 40 characters, when the post is a poll
- **Poll ends** — when voting closes, one to seven days after publishing
- **Poll results** — how many votes each option has
- **Channel** — the channel the post was shared in, if any; only the first post of a thread has one
- **Thread** — the earlier post of the same thread this one continues, for the second to tenth post of a thread
- **Pinned** — whether the post is pinned to the top of its author's profile
- **Views** — how many times the post was seen

## States

### Published

Visible on its author's profile and in the feeds.

### Deleted

Deleted by its author; shown nowhere.
