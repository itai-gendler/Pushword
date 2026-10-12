---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "restore-version",
      "contexts": [
        {
          "place": "administration::editorial"
        }
      ]
    },
    {
      "type": "capability",
      "id": "edit-administrative-content",
      "contexts": [
        {
          "place": "administration::editorial"
        }
      ]
    },
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

# Version capture and restoration preserve their scalar contract

Configured version capture records scalar values, deduplicates by captured content and attributes the capture to the authorized write. Restoration applies captured columns without reconstructing uncaptured associations or creating an ordinary new restore snapshot. Comparison writes affect only their supported live fields; malformed properties YAML can warn while other valid fields save.
