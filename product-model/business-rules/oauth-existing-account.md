---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "sign-in",
      "contexts": [
        {
          "place": "administration::login"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Security/OAuthAuthenticator.php"
    }
  ]
}
---

# OAuth matches an existing profile email

Configured OAuth signs in only an existing profile matched by the provider email. An unmatched email is not automatic registration.
