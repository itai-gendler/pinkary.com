---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "profile",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Http/Controllers/QrCodeController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Services/QrCode.php"
    }
  ]
}
---

# Download QR code

A User downloads a QR code image of their profile address, light or dark.
