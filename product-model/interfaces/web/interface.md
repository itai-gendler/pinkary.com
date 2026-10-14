---
{
  "type": "web",
  "actors": [
    "guest",
    "user"
  ],
  "languages": [
    "en"
  ],
  "entryPoints": [
    {
      "web": "/"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "routes/web.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "routes/auth.php"
    }
  ]
}
---

# Web

Pinkary at pinkary.com: public profiles, posts and feeds, and the signed-in pages where Users manage their profile and take part.
