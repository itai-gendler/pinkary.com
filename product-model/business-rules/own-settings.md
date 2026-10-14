---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "user",
      "effect": "changes",
      "facts": [
        "Name",
        "Username",
        "Email",
        "Email verified at",
        "Password",
        "Bio",
        "Avatar",
        "Avatar uploaded",
        "GitHub username",
        "Mail preference",
        "Default feed",
        "Ask anonymously by default",
        "Who can ask questions",
        "Link shape",
        "Link color",
        "Link order",
        "Two-factor authentication",
        "Recovery codes"
      ]
    }
  ],
  "permits": [
    {
      "self": true
    },
    {
      "actors": [
        "guest"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Http/Controllers/UserController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Http/Controllers/Auth/NewPasswordController.php"
    }
  ]
}
---

# Only a User changes their own profile and account settings

Name, username, email, bio, preferences, avatar, links' look and order, GitHub connection, password and two-factor settings change only through the User themselves, signed in or, for the password, through the reset link sent to their email.
