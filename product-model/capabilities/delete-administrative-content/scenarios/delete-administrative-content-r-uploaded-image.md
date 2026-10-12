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
      "text": "Request removal through the selected stronger administration process.",
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
      "text": "The selected uploader media is removed along with applicable storage and relationships.",
      "entities": [
        {
          "entity": "image",
          "effect": "removes"
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
      "target": "packages/template-editor/src/ElementAdmin.php"
    }
  ]
}
---

# Delete administrative content — uploaded image

## Trigger

Delete administrative content through editorial administration using the uploaded image way.

## Outcome

The selected uploader media is removed along with applicable storage and relationships.
