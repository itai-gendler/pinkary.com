---
{
  "kind": "person",
  "acts": "external",
  "relations": [
    {
      "entity": "link",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "question",
      "verb": "asks",
      "cardinality": "one-to-many"
    },
    {
      "entity": "question",
      "verb": "receives",
      "cardinality": "one-to-many"
    },
    {
      "entity": "post",
      "verb": "writes",
      "cardinality": "one-to-many"
    },
    {
      "entity": "comment",
      "verb": "writes",
      "cardinality": "one-to-many"
    },
    {
      "entity": "like",
      "verb": "gives",
      "cardinality": "one-to-many"
    },
    {
      "entity": "bookmark",
      "verb": "saves",
      "cardinality": "one-to-many"
    },
    {
      "entity": "repost",
      "verb": "makes",
      "cardinality": "one-to-many"
    },
    {
      "entity": "follow",
      "verb": "starts",
      "cardinality": "one-to-many"
    },
    {
      "entity": "follow",
      "verb": "is-followed-through",
      "cardinality": "one-to-many"
    },
    {
      "entity": "vote",
      "verb": "casts",
      "cardinality": "one-to-many"
    },
    {
      "entity": "notification",
      "verb": "receives",
      "cardinality": "one-to-many"
    },
    {
      "entity": "switcher-entry",
      "verb": "is-listed-as",
      "cardinality": "one-to-many"
    },
    {
      "entity": "channel",
      "verb": "creates",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Models/User.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Http/Requests/UserUpdateRequest.php"
    }
  ]
}
---

# User

A person with a Pinkary account: a profile page with their links, questions others ask them, their posts and the people they follow.

## Information kept

- **Name** — the display name shown on the profile and beside every post
- **Username** — the unique handle that addresses the profile at /@username
- **Email** — the address used to log in and to receive verification, reset and notification emails
- **Email verified at** — when the email address was confirmed through the emailed link; empty until then and again after the email changes
- **Password** — the secret used to log in
- **Bio** — a short text of up to 255 characters shown on the profile, with links and mentions made clickable
- **Avatar** — the profile picture, either uploaded or fetched from GitHub or Gravatar
- **Avatar uploaded** — whether the current avatar is one the User uploaded rather than a fetched one
- **GitHub username** — the connected GitHub account, unique across users
- **Verified** — whether the User shows the verified badge, earned by sponsoring Pinkary on GitHub
- **Company verified** — whether the User shows the company verified badge, earned by a company sponsorship
- **Mail preference** — how often unread notifications are emailed: Daily, Weekly or Never
- **Default feed** — which feed Home opens: Recent, Following or Trending
- **Ask anonymously by default** — whether questions the User asks start out anonymous
- **Who can ask questions** — who may ask this User a question: Everyone, Following (only people the User follows) or No one
- **Link shape** — the shape of the link buttons on the profile: square, rounded or pill
- **Link color** — the color gradient of the link buttons on the profile, one of six
- **Link order** — the order the User arranged their links in
- **Profile views** — how many times the profile was viewed
- **Two-factor authentication** — whether a one-time code from an authenticator app is required at log in, and whether its setup is confirmed
- **Recovery codes** — single-use codes that replace the authenticator code at log in
