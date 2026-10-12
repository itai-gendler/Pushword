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
      "text": "Request reconciliation of the specified scope.",
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
      "text": "An active webhook lock in the supplied/default scope blocks reconciliation before host iteration.",
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

# Synchronize pages — webhook lock

## Trigger

Synchronize pages through operator CLI using the webhook lock way.

## Outcome

An active webhook lock in the supplied/default scope blocks reconciliation before host iteration.
