---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens their own profile",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Name",
            "Username",
            "Avatar",
            "Bio",
            "Profile views",
            "Link shape",
            "Link color",
            "Link order"
          ]
        },
        {
          "entity": "link",
          "effect": "reads",
          "facts": [
            "Description",
            "URL",
            "Clicks"
          ]
        },
        {
          "entity": "question",
          "effect": "reads",
          "facts": [
            "Question text",
            "Anonymous",
            "Answer",
            "Answered at",
            "Views",
            "Pinned"
          ]
        },
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Content",
            "Images",
            "Published at",
            "Poll options",
            "Poll results",
            "Channel",
            "Views",
            "Pinned"
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

# A User views their own profile

## Trigger

A User opens their own profile.

## Outcome

The User sees their hidden links with click counts and the questions still waiting for an answer, besides what everyone sees.
