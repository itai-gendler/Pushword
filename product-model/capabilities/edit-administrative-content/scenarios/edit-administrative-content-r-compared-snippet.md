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
      "text": "Submit the selected source, comparison or uploader changes.",
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
      "text": "Accepted supported comparison fields are written to the live subject and the actor is carried to its ordinary editing context. Installed version capture retains the resulting distinct scalar snapshot.",
      "entities": [
        {
          "entity": "snippet",
          "effect": "changes",
          "facts": [
            "Content",
            "Name",
            "Slug",
            "Custom properties"
          ]
        },
        {
          "entity": "snippet-version",
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

# Edit administrative content — compared snippet

## Trigger

Edit administrative content through editorial administration using the compared snippet way.

## Outcome

Accepted supported comparison fields are written to the live subject and the actor is carried to its ordinary editor.
