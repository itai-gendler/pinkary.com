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
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Models/Question.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Policies/QuestionPolicy.php"
    }
  ]
}
---

# Question

A question one User asks another, answered on the recipient's profile.

## Information kept

- **Question text** — what was asked, up to 255 characters
- **Anonymous** — whether the asker is hidden from everyone, the recipient included
- **Asked at** — when the question was sent
- **Answer** — the recipient's answer, up to 1000 characters, with links, mentions, hashtags, code and images
- **Answered at** — when the answer was first given
- **Answer edited at** — when the answer was last edited
- **Pinned** — whether the answered question is pinned to the top of the recipient's profile
- **Views** — how many times the answer was seen

## States

### Unanswered

Waiting for the recipient, visible only to them.

### Answered

Visible on the recipient's profile and in the feeds.

### Ignored

Ignored or deleted by the recipient; shown nowhere.

### Reported

Reported by the recipient; shown nowhere.
