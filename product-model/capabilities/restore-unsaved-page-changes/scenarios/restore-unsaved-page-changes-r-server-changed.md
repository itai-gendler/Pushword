---
{
  "kind": "edge",
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
      "text": "A changed server baseline produces the recovery conflict notice; applying a browser copy remains a form operation, not an automatic overwrite.",
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

# Restore unsaved page changes — server changed

## Trigger

Restore unsaved page changes through editorial administration using the server changed way.

## Outcome

A changed server baseline produces the recovery conflict notice; applying a browser copy remains a form operation, not an automatic overwrite.
