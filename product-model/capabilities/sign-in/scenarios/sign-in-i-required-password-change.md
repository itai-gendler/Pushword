---
{
  "kind": "edge",
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
      "text": "A successful access method with required password completion masks ordinary privileges and carries the person to password completion.",
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

# Sign in — required password change

## Trigger

Sign in through login using the required password change way.

## Outcome

A successful access method with required password completion masks ordinary privileges and carries the person to password completion.
