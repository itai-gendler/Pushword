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
      "text": "Request removal through the selected stronger administration process.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::template"
        }
      },
      "capability": "delete-administrative-content"
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "Confirmed deletion removes the selected source and carries the actor to the retained collection.",
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
      },
      "capability": "delete-administrative-content"
    },
    {
      "kind": "product",
      "actor": "administrator",
      "capability": "delete-administrative-content",
      "text": "The Product carries the person to the editable-source collection.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::template"
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
          "place": "administration::editorial::templates"
        }
      },
      "capability": "browse-administrative-content"
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "The selected editable source paths are returned; the shipped unrestricted override clears ordinary selection restrictions.",
      "entities": [
        {
          "entity": "template",
          "effect": "reads",
          "facts": [
            "Path",
            "Source"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::templates"
        }
      },
      "capability": "browse-administrative-content"
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
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/VersionController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/template-editor/src/ElementRepository.php"
    }
  ]
}
---

# Return to templates — deleted

## Trigger

Return to the editable-source collection after removal.

## Outcome

The selected source is removed and the editable-source collection is presented.
