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
      "text": "End the current session.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The current CMS session ends at its existing authenticated context.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Resources/config/packages/security.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Resources/assets/admin.unsavedChanges.js"
    }
  ]
}
---

# Sign out — end session

## Trigger

Sign out through editorial administration using the end session way.

## Outcome

The current CMS session ends at its existing authenticated context.
