---
{
  "kind": "primary",
  "routes": {
    "main": "Login"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "user",
      "text": "Supply the selected access method’s input.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::login::sign-in"
        }
      }
    },
    {
      "kind": "product",
      "actor": "user",
      "text": "The valid unused access link for the existing profile is consumed and establishes access.",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Email",
            "Roles",
            "Password change required"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::login::sign-in"
        }
      }
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
      "target": "packages/core/src/Security/LoginFormAuthenticator.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Security/MagicLinkAuthenticator.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Security/OAuthAuthenticator.php"
    }
  ]
}
---

# Sign in — magic link

## Trigger

Sign in through login using the magic link way.

## Outcome

The valid unused access link for the existing profile is consumed and establishes access.
