---
{
  "kind": "primary",
  "routes": {
    "main": "Account"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "user",
      "text": "Submit the replacement credential and confirmation.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::account::password"
        }
      }
    },
    {
      "kind": "product",
      "actor": "user",
      "text": "Confirmed valid replacement stores the credential and clears the required-change flag.",
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
          "place": "administration::account::password"
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

# Change password — required change

## Trigger

Change password through own account using the required change way.

## Outcome

Confirmed valid replacement stores the credential and clears the required-change flag.
