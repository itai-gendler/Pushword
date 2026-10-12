---
{
  "kind": "edge",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "administrator",
      "text": "Open the selected historical comparison.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::comparison"
        }
      }
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "For held content the latest non-held snapshot is used, or the oldest available fallback; this does not establish live served output.",
      "entities": [
        {
          "entity": "page",
          "effect": "reads",
          "facts": [
            "Content",
            "Slug",
            "Heading",
            "Title",
            "Custom properties"
          ]
        },
        {
          "entity": "page-version",
          "effect": "reads",
          "facts": [
            "Version reference",
            "Captured values"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::comparison"
        }
      }
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

# Compare versions — held baseline

## Trigger

Compare versions through editorial administration using the held baseline way.

## Outcome

For held content the latest non-held snapshot is used, or the oldest available fallback; this does not establish live served output.
