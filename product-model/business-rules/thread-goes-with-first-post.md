---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "post",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "writes",
          "entity": "user"
        }
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

# Later posts of a thread are removed only with an earlier post of the thread

Deleting a post removes the posts that continue it.
