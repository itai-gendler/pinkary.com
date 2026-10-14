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
      "target": "app/Actions/Users/CreateFollow.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Livewire/Concerns/Followable.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Policies/UserPolicy.php#follow"
    }
  ]
}
---

# Follow user

A User follows another User from their profile, a people list or the suggestions.
