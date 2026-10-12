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
      "text": "The ordinary operator manual-lock path can replace a non-manual active lock.",
      "entities": [
        {
          "entity": "editorial-lock",
          "effect": "changes",
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

# Lock flat edits — non manual overridden

## Trigger

Lock flat edits through operator CLI using the non manual overridden way.

## Outcome

The ordinary operator manual-lock path can replace a non-manual active lock.
