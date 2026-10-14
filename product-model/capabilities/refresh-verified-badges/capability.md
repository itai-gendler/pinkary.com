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
      "target": "app/Console/Commands/SyncVerifiedUsersCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Jobs/SyncVerifiedUser.php"
    }
  ]
}
---

# Refresh verified badges

Every day the Product checks with GitHub that verified Users still sponsor Pinkary and updates their badges.
