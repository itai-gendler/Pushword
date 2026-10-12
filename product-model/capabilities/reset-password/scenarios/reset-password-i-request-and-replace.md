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
      "text": "Request replacement and follow the supplied reset link.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::login::password"
        }
      }
    },
    {
      "kind": "product",
      "actor": "user",
      "text": "The enabled own-account request sends its bound reset link; valid completion stores the replacement credential and consumes the link.",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Password",
            "Password change required"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::login::password"
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
      "target": "packages/core/src/Service/MagicLinkMailer.php"
    }
  ]
}
---

# Reset password — request and replace

## Trigger

Reset password through login using the request and replace way.

## Outcome

The enabled own-account request sends its bound reset link; valid completion stores the replacement credential and consumes the link.
