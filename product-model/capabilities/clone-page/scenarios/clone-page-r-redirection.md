---
{
  "kind": "primary",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Request a draft copy of the selected content.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::redirection"
        }
      }
    },
    {
      "kind": "condition",
      "text": "Version capture is installed and enabled. This accepted write produces distinct scalar values; retained earlier snapshots are inside the full-retention interval.",
      "entities": [
        {
          "entity": "product-settings",
          "effect": "reads",
          "facts": [
            "Installed extensions"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::redirection"
        }
      },
      "actor": "editor"
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "A redirect-only copy is created with publication cleared and a copy address, and the editing context is carried to it; fallback redirect eligibility remains separate. Installed version capture retains the resulting distinct scalar snapshot.",
      "entities": [
        {
          "entity": "redirection",
          "effect": "creates",
          "facts": [
            "Reference",
            "Host",
            "Slug",
            "Destination",
            "Response code",
            "Heading",
            "Locale",
            "Publication date",
            "Hold date",
            "Created at",
            "Updated at",
            "Tags",
            "Weight",
            "Custom properties",
            "Redirect paths",
            "Creator",
            "Last editor"
          ]
        },
        {
          "entity": "page-version",
          "effect": "creates",
          "facts": [
            "Version reference",
            "Captured at",
            "Captured editor",
            "Captured values"
          ],
          "with": "redirection"
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::redirection"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/PageCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Service/VariantManager.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/Versionner.php"
    }
  ]
}
---

# Clone page — redirection

## Trigger

Clone page through editorial administration using the redirection way.

## Outcome

A redirect-only copy is created with publication cleared and a copy address, and the editor is carried to it; fallback redirect eligibility remains separate.
