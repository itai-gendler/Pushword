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
      "text": "Invalid, expired, consumed or wrong-purpose setup proof does not change credentials.",
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
    }
  ]
}
---

# Change password — invalid link

## Trigger

Change password through login using the invalid link way.

## Outcome

Invalid, expired, consumed or wrong-purpose setup proof does not change credentials.
