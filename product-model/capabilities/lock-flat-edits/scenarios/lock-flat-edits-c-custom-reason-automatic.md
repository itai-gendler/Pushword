---
{
  "kind": "edge",
  "routes": {
    "main": "Operator CLI"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "site-operator",
      "text": "Supply the requested editing scope, reason and holder.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "operator-cli"
        }
      }
    },
    {
      "kind": "product",
      "actor": "site-operator",
      "text": "A supplied custom reason can classify the newly retained operator lock as automatic rather than manual.",
      "entities": [
        {
          "entity": "editorial-lock",
          "effect": "creates",
          "facts": [
            "Scope",
            "Kind",
            "Reason",
            "Acquired at",
            "TTL",
            "Locked by"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "operator-cli"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Controller/FlatLockApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Command/FlatLockCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Service/FlatLockManager.php"
    }
  ]
}
---

# Lock flat edits — custom reason automatic

## Trigger

Lock flat edits through operator CLI using the custom reason automatic way.

## Outcome

A supplied custom reason can classify the newly retained operator lock as automatic rather than manual.
