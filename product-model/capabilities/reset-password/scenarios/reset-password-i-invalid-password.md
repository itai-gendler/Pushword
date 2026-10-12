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
      "text": "A replacement shorter than seven characters or not matching its confirmation is not stored.",
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

# Reset password — invalid password

## Trigger

Reset password through login using the invalid password way.

## Outcome

A replacement shorter than seven characters or not matching its confirmation is not stored.
