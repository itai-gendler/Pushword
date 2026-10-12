---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "redirection",
      "effect": "changes",
      "contexts": [
        {
          "place": "operator-cli::page-transfer"
        }
      ]
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
      "target": "packages/flat/src/FlatFileSync.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Service/FlatLockManager.php"
    }
  ]
}
---

# Redirection transfer changes stop when the command scope has an active webhook lock

Before ordinary import, export or synchronization performs Redirection changes, the Product checks the webhook lock for the command-supplied host. An omitted or empty host selects the literal default lock scope after normalization. An active webhook lock stops the transfer before content operations; Force does not bypass the check.

For all-host transfer, this preflight checks the supplied/default command scope before host iteration. It is not repeated for each affected record’s Host or configured Site. This concurrency constraint retains the independent Site operator grants; it does not derive authority from a Site or record owner.
