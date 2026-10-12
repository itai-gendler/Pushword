---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "lock-flat-edits",
      "contexts": [
        {
          "place": "cms-api::editorial"
        },
        {
          "place": "operator-cli"
        }
      ]
    },
    {
      "type": "capability",
      "id": "unlock-flat-edits",
      "contexts": [
        {
          "place": "cms-api::editorial"
        },
        {
          "place": "operator-cli"
        }
      ]
    },
    {
      "type": "capability",
      "id": "read-api-status",
      "contexts": [
        {
          "place": "cms-api::editorial"
        }
      ]
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
      "target": "packages/flat/src/Service/FlatApiTokenValidator.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Service/FlatLockManager.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Command/FlatLockCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Command/FlatUnlockCommand.php"
    }
  ]
}
---

# Lock behavior follows normalized scope, requested operation and kind

Lock scope comes from the normalized storage key. Omitted or empty host uses the literal default key; other hosts replace characters outside [a-zA-Z0-9_-] with underscores. Distinct raw hosts can collide. The key need not identify a configured Site.

Explicit API release reads the raw lock and refuses any existing non-webhook kind, including an expired manual lock, without first expiring it. An absent lock succeeds without a retained removal. Status checking removes an existing lock of any kind only when the check’s clock is strictly later than Acquired at plus TTL. Expiry alone does not establish immediate deletion or autonomous processing: cleanup occurs during a lock check.

API acquisition refuses an active webhook lock. It can replace another kind or an expired record directly without a preliminary deletion. Operator manual acquisition has its separate override behavior; a custom CLI reason can classify acquisition as automatic, which cannot overwrite an active manual or webhook lock. CLI release can remove any kind. The lock is not owner-only.
