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
      "text": "Unavailable origin-local storage prevents durable recovery while leaving ordinary form editing available.",
      "entities": [],
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

# Restore unsaved page changes — storage unavailable

## Trigger

Restore unsaved page changes through editorial administration using the storage unavailable way.

## Outcome

Unavailable origin-local storage prevents durable recovery while leaving ordinary form editing available.
