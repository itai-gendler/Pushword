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
    },
    {
      "type": "capability",
      "id": "reset-password",
      "contexts": [
        {
          "place": "administration::login"
        }
      ]
    },
    {
      "type": "capability",
      "id": "change-password",
      "contexts": [
        {
          "place": "administration::account"
        },
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
      "target": "packages/core/src/Controller/UserController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Entity/User.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Service/MagicLinkMailer.php"
    }
  ]
}
---

# Access links bind account purpose expiry and use

Access links bind to an existing profile, purpose, expiry and use. A valid one-use link is consumed through its applicable completion path; wrong-purpose, expired or consumed proof does not gain an alternate credential contract.
