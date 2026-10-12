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
      "text": "When no usable baseline is available the actor is carried to the historical collection instead of a comparison result.",
      "entities": [
        {
          "entity": "page",
          "effect": "reads",
          "facts": [
            "Reference",
            "Host",
            "Slug",
            "Heading",
            "Title",
            "Content",
            "Locale",
            "Publication date",
            "Hold date",
            "Tags",
            "Weight",
            "Custom properties"
          ]
        },
        {
          "entity": "page-version",
          "effect": "reads",
          "facts": [
            "Version reference",
            "Captured at",
            "Captured editor",
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

# Compare versions — no history routing

## Trigger

Compare versions through editorial administration using the no history routing way.

## Outcome

When no usable baseline is available the actor is carried to the historical collection instead of a comparison result.
