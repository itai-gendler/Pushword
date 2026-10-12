---
{
  "kind": "primary",
  "routes": {
    "main": "Account"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "user",
      "text": "End the current session.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::account"
        }
      }
    },
    {
      "kind": "product",
      "actor": "user",
      "text": "The current CMS session ends at its existing authenticated context.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::account"
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

Sign out through own account using the end session way.

## Outcome

The current CMS session ends at its existing authenticated context.
