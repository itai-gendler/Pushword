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
      "text": "Discard the selected origin-local recovery copy.",
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
      "text": "The selected editing context-and-subject browser copy is removed without changing persisted content.",
      "entities": [
        {
          "entity": "browser-draft",
          "effect": "removes"
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
    }
  ]
}
---

# Discard unsaved page changes — copy removed

## Trigger

Discard unsaved page changes through editorial administration using the copy removed way.

## Outcome

The selected editor-and-subject browser copy is removed without changing persisted content.
