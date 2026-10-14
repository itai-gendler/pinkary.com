---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User changes their name, username, bio and preferences and saves",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Name",
            "Username",
            "Email",
            "Bio",
            "Mail preference",
            "Default feed",
            "Ask anonymously by default",
            "Who can ask questions"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::settings"
        }
      }
    },
    {
      "text": "The Product saves the profile information",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Name",
            "Username",
            "Bio",
            "Mail preference",
            "Default feed",
            "Ask anonymously by default",
            "Who can ask questions"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::settings"
        }
      }
    }
  ]
}
---

# Save profile information

## Trigger

A User changes how their profile looks or behaves.

## Outcome

The profile shows the new information and the preferences apply from now on.
