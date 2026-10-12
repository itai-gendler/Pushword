---
{
  "kind": "primary",
  "routes": {
    "main": "CMS API"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Supply the requested editing scope, reason and holder.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "cms-api::editorial"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "A lock is retained at the normalized requested scope with its reason, holder and expiry information.",
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
          "place": "cms-api::editorial"
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

# Lock flat edits — acquire

## Trigger

Lock flat edits through editorial API using the acquire way.

## Outcome

A lock is retained at the normalized requested scope with its reason, holder and expiry information.
