---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "link",
      "effect": "creates"
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
      "target": "app/Livewire/Links/Create.php"
    }
  ]
}
---

# Only a signed-in User adds links to their profile, up to 10, or 20 when verified

Links point to https addresses of up to 100 characters with descriptions of up to 100 characters.
