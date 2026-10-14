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
      "target": "app/Livewire/Questions/Create.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Observers/QuestionObserver.php"
    }
  ]
}
---

# Comment

A reply a User writes under a post, an answered question or another comment.

## Information kept

- **Content** — the text, up to 1000 characters, with links, mentions, hashtags and code
- **Images** — up to three images placed in the content
- **Published at** — when the comment was written
- **Edited at** — when the comment was last edited
- **Poll options** — two to four options of up to 40 characters, when the comment is a poll
- **Poll ends** — when voting closes
- **Poll results** — how many votes each option has
- **Views** — how many times the comment was seen

## States

### Published

Visible under what it replies to.

### Deleted

Deleted by its author; shown nowhere.
