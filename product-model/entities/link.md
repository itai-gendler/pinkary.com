---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Models/Link.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Livewire/Links/Index.php"
    }
  ]
}
---

# Link

One link on a User's profile page.

## Information kept

- **Description** — the label shown on the link button, up to 100 characters
- **URL** — the https address the link opens, up to 100 characters
- **Clicks** — how many distinct visitors opened the link, counted at most once a day per visitor

## States

### Visible

Shown to everyone on the profile.

### Hidden

Shown only to its owner, who can show it again.
