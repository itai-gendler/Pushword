---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "compare-versions",
      "contexts": [
        {
          "place": "administration::editorial"
        }
      ]
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

# Comparison shortcuts select a historical baseline

Held content compares with the latest non-held snapshot or the oldest fallback; other content uses a distinct previous snapshot or the oldest fallback. Missing usable history redirects to its collection. The shortcut compares the selected historical baseline with current live values by default; explicit comparison can select another snapshot. A baseline is historical selection, not proof of currently served output.
