---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "comment",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "actors": [
        "user"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Observers/QuestionObserver.php#deleted"
    }
  ]
}
---

# Comments are removed only along with what they reply to

Deleting a post, an answer or a comment removes the comments under it, and deleting a thread's first post removes the later posts of the thread; nobody removes someone else's comment directly.
