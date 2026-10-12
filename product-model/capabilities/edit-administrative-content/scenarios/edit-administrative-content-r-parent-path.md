---
{
  "kind": "validation",
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
          "place": "administration::editorial::template"
        }
      }
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "A proposed path containing parent traversal is refused.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::template"
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
    }
  ]
}
---

# Edit administrative content — parent path

## Trigger

Edit administrative content through editorial administration using the parent path way.

## Outcome

A proposed path containing parent traversal is refused.
