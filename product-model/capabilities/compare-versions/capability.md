---
{
  "availability": [
    {
      "place": "administration::editorial"
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

# Compare versions

Inspect selected scalar snapshots against the historical baseline or follow the no-baseline history fallback.

## Established boundaries

- The selected comparison can disclose a historical snapshot against current live values or a separately selected historical snapshot; shortcut baseline selection does not identify current deployed output.
