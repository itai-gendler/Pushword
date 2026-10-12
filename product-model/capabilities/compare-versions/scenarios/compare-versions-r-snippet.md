---
{
  "kind": "primary",
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
      "text": "The selected historical scalar values are compared with current live values by default, or another explicitly selected snapshot. The comparison is not proof of deployed output.",
      "entities": [
        {
          "entity": "snippet",
          "effect": "reads",
          "facts": [
            "Content",
            "Slug",
            "Name",
            "Custom properties"
          ]
        },
        {
          "entity": "snippet-version",
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

# Compare versions — snippet

## Trigger

Compare versions through editorial administration using the snippet way.

## Outcome

The selected historical scalar values are compared with current live values by default, or another explicitly selected snapshot. The comparison is not proof of deployed output.
