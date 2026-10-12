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
          "place": "administration::editorial::redirection"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The selected redirect-only editing context’s browser copy is removed without changing persisted content.",
      "entities": [
        {
          "entity": "browser-draft",
          "effect": "removes"
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::redirection"
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

# Discard unsaved page changes — redirection copy removed

## Trigger

Discard unsaved page changes through editorial administration using the redirection copy removed way.

## Outcome

The selected redirect-only editor’s browser copy is removed without changing persisted content.
