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
          "place": "administration::editorial::multiple-upload"
        }
      }
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "Accepted uploader descriptive, naming and licensing values are saved.",
      "entities": [
        {
          "entity": "image",
          "effect": "changes",
          "facts": [
            "Filename",
            "Filename history",
            "Alternative text",
            "Localized text",
            "Tags",
            "Rights values",
            "Licensing origin",
            "Custom properties"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::multiple-upload"
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

# Edit administrative content — uploaded image

## Trigger

Edit administrative content through editorial administration using the uploaded image way.

## Outcome

Accepted uploader descriptive, naming and licensing values are saved.
