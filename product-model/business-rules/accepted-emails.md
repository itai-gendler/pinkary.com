---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "register-account"
    },
    {
      "type": "capability",
      "id": "edit-profile"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Rules/NoEmailAlias.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Rules/UnauthorizedEmailProviders.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Rules/NotBlockedAccount.php"
    }
  ]
}
---

# An email is accepted only when it is not an alias, not from a refused provider and not blocked

Registration and profile changes refuse addresses with an alias part, addresses from refused providers, and, at registration, addresses the Pinkary team blocked.
