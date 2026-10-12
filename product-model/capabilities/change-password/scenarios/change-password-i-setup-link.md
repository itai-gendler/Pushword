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
      "text": "Submit the replacement credential and confirmation.",
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
      "text": "A valid setup-purpose link completes the bound profile’s password setup; the forgot-password request setting is not imposed on this link handler.",
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
    }
  ]
}
---

# Change password — setup link

## Trigger

Change password through login using the setup link way.

## Outcome

A valid setup-purpose link completes the bound profile’s password setup; the forgot-password request setting is not imposed on this link handler.
