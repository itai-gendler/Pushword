---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "page-version"
    },
    {
      "type": "entity",
      "id": "snippet-version"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/VersionController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/Versionner.php"
    }
  ]
}
---

# Snapshot age determines daily and weekly retention

Retention keeps all snapshots younger than thirty days, the newest per day from thirty through ninety days and the newest per week thereafter. Names whose date cannot be interpreted are retained. Clearing through the guarded route is separate from automatic pruning.
