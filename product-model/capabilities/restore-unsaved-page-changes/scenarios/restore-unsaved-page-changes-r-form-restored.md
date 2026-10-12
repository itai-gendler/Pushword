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
      "text": "Apply the selected origin-local recovery copy.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::page"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "Recoverable changed fields are restored into the selected form without saving database content.",
      "entities": [
        {
          "entity": "browser-draft",
          "effect": "reads",
          "facts": [
            "Changed fields",
            "Baseline",
            "Saved at"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::page"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Resources/assets/admin.unsavedChanges.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/templates/page/edit.html.twig"
    }
  ]
}
---

# Restore unsaved page changes — form restored

## Trigger

Restore unsaved page changes through editorial administration using the form restored way.

## Outcome

Recoverable changed fields are restored into the selected form without saving database content.
