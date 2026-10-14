---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Console/Commands/DeleteNonEmailVerifiedUsersCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "routes/console.php"
    }
  ]
}
---

# Remove unverified accounts

Every hour the Product deletes accounts whose email stayed unverified for a day and that have no links, questions or posts older than a day.
