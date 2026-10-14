---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "settings",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Livewire/Profile/TwoFactorAuthenticationForm.php#TwoFactorAuthenticationForm"
    }
  ]
}
---

# Enable two-factor authentication

A User turns on two-factor authentication: after confirming their password they scan the setup key into an authenticator app and confirm it with a code, then see their recovery codes.
