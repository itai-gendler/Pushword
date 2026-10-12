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
      "text": "A disabled reset-request setting refuses the request.",
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

# Reset password — disabled

## Trigger

Reset password through login using the disabled way.

## Outcome

A disabled reset-request setting refuses the request.
