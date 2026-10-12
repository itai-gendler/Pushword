---
{
  "kind": "primary",
  "result": "achieved",
  "routes": {
    "main": "Product hand-off"
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
      },
      "capability": "compare-versions"
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
      },
      "capability": "compare-versions"
    },
    {
      "kind": "product",
      "actor": "administrator",
      "capability": "compare-versions",
      "text": "The Product carries the person to the subject history because no usable baseline exists.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::comparison"
        }
      }
    },
    {
      "kind": "actor",
      "actor": "administrator",
      "text": "Request the selected historical or editable-source collection.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::versions"
        }
      },
      "capability": "browse-administrative-content"
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "The historical collection is presented without inventing a missing comparison baseline.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::versions"
        }
      },
      "capability": "browse-administrative-content"
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
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/template-editor/src/ElementRepository.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/template-editor/src/ElementAdmin.php"
    }
  ]
}
---

# Inspect history without baseline — empty history

## Trigger

Inspect the selected subject’s history when no comparison baseline exists.

## Outcome

The no-baseline redirect presents the historical collection, including its empty outcome.
