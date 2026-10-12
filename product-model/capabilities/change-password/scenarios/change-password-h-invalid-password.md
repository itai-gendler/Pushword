---
{
  "kind": "validation",
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
      "text": "A replacement shorter than seven characters or with a different confirmation does not complete password change.",
      "entities": [],
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

# Change password — invalid password

## Trigger

Change password through own account using the invalid password way.

## Outcome

A replacement shorter than seven characters or with a different confirmation does not complete password change.
