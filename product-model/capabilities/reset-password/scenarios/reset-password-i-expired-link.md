---
{
  "kind": "validation",
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
      "text": "Expired replacement proof does not replace the credential.",
      "entities": [],
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

# Reset password — expired link

## Trigger

Reset password through login using the expired link way.

## Outcome

Expired replacement proof does not replace the credential.
