---
{
  "relations": [
    {
      "entity": "post",
      "verb": "tags",
      "cardinality": "many-to-many"
    },
    {
      "entity": "question",
      "verb": "tags",
      "cardinality": "many-to-many"
    },
    {
      "entity": "comment",
      "verb": "tags",
      "cardinality": "many-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Actions/Questions/UpdateQuestionHashtags.php"
    }
  ]
}
---

# Hashtag

A #tag written in a post, answer or comment, with a page listing what carries it.

## Information kept

- **Name** — the tag without its #, letters and digits only
