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
      "text": "Request the selected historical or editable-source collection.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::templates"
        }
      }
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

# Browse administrative content — templates

## Trigger

Browse administrative content through editorial administration using the templates way.

## Outcome

The selected editable source paths are returned; the shipped unrestricted override clears ordinary selection restrictions.
