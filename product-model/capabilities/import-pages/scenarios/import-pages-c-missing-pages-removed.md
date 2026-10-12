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
      "text": "Request the specified filesystem-to-database transfer.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "operator-cli::page-transfer"
        }
      }
    },
    {
      "kind": "product",
      "actor": "site-operator",
      "text": "A full import removes applicable database content absent from the stored asset; targeted import does not perform this sweep.",
      "entities": [
        {
          "entity": "page",
          "effect": "removes",
          "from": "Published"
        },
        {
          "entity": "redirection",
          "effect": "removes"
        }
      ],
      "contexts": {
        "main": {
          "place": "operator-cli::page-transfer"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Command/FlatFileSyncCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Sync/PageSync.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Service/FlatLockManager.php"
    }
  ]
}
---

# Import pages — missing pages removed

## Trigger

Import pages through operator CLI using the missing pages removed way.

## Outcome

A full import removes applicable database content absent from the files; targeted import does not perform this sweep.
