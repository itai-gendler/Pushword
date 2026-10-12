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
      "text": "Following the administration logout link removes all matching origin-local unsaved copies; session expiry alone does not do this.",
      "entities": [
        {
          "entity": "browser-draft",
          "effect": "removes"
        }
      ],
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

# Sign out — browser copies cleared

## Trigger

Sign out through editorial administration using the browser copies cleared way.

## Outcome

Following the administration logout link removes all matching origin-local unsaved copies; session expiry alone does not do this.
