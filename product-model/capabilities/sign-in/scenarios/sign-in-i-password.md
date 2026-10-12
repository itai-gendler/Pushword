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
      "text": "Valid password credentials establish access to the existing profile.",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Email",
            "Roles",
            "Password change required",
            "Password"
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

# Sign in — password

## Trigger

Sign in through login using the password way.

## Outcome

Valid password credentials establish access to the existing profile.
