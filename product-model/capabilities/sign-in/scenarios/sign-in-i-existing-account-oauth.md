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
      "text": "A configured provider’s authenticated email matches an existing profile and establishes access; no registration is inferred.",
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

# Sign in — existing account oauth

## Trigger

Sign in through login using the existing account oauth way.

## Outcome

A configured provider’s authenticated email matches an existing profile and establishes access; no registration is inferred.
