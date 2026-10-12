---
{
  "kind": "validation",
  "routes": {
    "main": "CMS API"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Request release of the specified editing scope.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "cms-api::editorial"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The Product reads the existing raw lock’s Kind without an expiry check.",
      "entities": [
        {
          "entity": "editorial-lock",
          "effect": "reads",
          "facts": [
            "Kind"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "cms-api::editorial"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "Explicit API release refuses the existing expired manual lock; no expiry cleanup or removal occurs.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "cms-api::editorial"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Controller/FlatLockApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Command/FlatUnlockCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Service/FlatLockManager.php"
    }
  ]
}
---

# Unlock flat edits — expired manual lock

## Trigger

An Editor requests explicit API release of an expired manual lock that remains stored because no prior expiry check has removed it.

## Outcome

The response refuses release with the existing lock information. The lock remains retained, including its expired timestamp; explicit release does not run lazy expiry first.
