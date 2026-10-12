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
      "text": "An unknown email receives the established nondisclosing request response without a link for another profile.",
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

# Reset password — unknown email

## Trigger

Reset password through login using the unknown email way.

## Outcome

An unknown email receives the established nondisclosing request response without a link for another profile.
