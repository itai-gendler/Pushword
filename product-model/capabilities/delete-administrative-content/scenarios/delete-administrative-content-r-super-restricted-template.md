---
{
  "kind": "primary",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "super-administrator",
      "text": "Request removal through the selected stronger administration process.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::template"
        }
      }
    },
    {
      "kind": "product",
      "actor": "super-administrator",
      "text": "The selected source is removed through the shipped unrestricted override even when ordinary creation restrictions are configured.",
      "entities": [
        {
          "entity": "template",
          "effect": "removes"
        }
      ],
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
      "target": "packages/template-editor/src/ElementAdmin.php"
    }
  ]
}
---

# Delete administrative content — super restricted template

## Trigger

Delete administrative content through editorial administration using the super restricted template way.

## Outcome

The selected source is removed through the shipped unrestricted override even when ordinary creation restrictions are configured.
