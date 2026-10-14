---
{
  "availability": [
    {
      "place": "web::public"
    },
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "profile",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Livewire/Links/Index.php#Index"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Actions/Links/UpdateLinkClicks.php"
    }
  ]
}
---

# Open link

Anyone opens a link on a profile; the click is counted for the link's owner.
