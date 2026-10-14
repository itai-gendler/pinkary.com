---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User uses the verification email while signed in",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::verify-email"
        }
      }
    },
    {
      "text": "The Product records the email as verified",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Email verified at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::verify-email"
        }
      }
    },
    {
      "text": "The Product opens the User's profile with a confirmation",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Username"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::profile"
        }
      }
    }
  ]
}
---

# Verify the email address

## Trigger

A User follows the verification link from their email.

## Outcome

The email is verified and the User lands on their own profile.
