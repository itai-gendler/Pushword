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
      "text": "Save changed body, heading and title with malformed unmanaged-properties YAML.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::comparison"
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
          "place": "administration::editorial::comparison"
        }
      },
      "actor": "administrator"
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "Malformed unmanaged-properties input produces its warning while other valid supported comparison fields can still be saved. Installed version capture retains the resulting distinct scalar snapshot.",
      "entities": [
        {
          "entity": "page",
          "effect": "changes",
          "facts": [
            "Content",
            "Heading",
            "Title",
            "Updated at",
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
      "target": "packages/admin/src/Controller/MediaMultiUploadController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/VersionController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/template-editor/src/ElementAdmin.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/template-editor/src/Element.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/Versionner.php"
    }
  ]
}
---

# Edit administrative content — invalid properties yaml

## Trigger

Edit administrative content through editorial administration using the invalid properties yaml way.

## Outcome

Malformed unmanaged-properties input produces its warning while other valid supported comparison fields can still be saved.
