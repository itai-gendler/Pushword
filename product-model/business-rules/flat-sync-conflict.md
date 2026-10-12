---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "synchronize-pages",
      "contexts": [
        {
          "place": "operator-cli"
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

# Later change times win and flat wins ties

When both sides changed since the remembered sync and content differs, the newer modification wins; equal times favor the flat representation. The observed backup copies the flat file and does not establish recovery of losing database body content.
