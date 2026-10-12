---
{
  "kind": "validation",
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
      "text": "An active webhook lock in the supplied/default scope blocks the command before host iteration.",
      "entities": [],
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

# Import pages — webhook lock

## Trigger

Import pages through operator CLI using the webhook lock way.

## Outcome

An active webhook lock in the supplied/default scope blocks the command before host iteration.
