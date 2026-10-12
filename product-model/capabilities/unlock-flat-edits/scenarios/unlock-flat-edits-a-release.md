---
{
  "kind": "primary",
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
      "text": "The Product verifies the existing raw lock has webhook Kind.",
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
      "text": "The selected lock is removed through this entry point’s release contract.",
      "entities": [
        {
          "entity": "editorial-lock",
          "effect": "removes"
        }
      ],
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

# Unlock flat edits — release

## Trigger

An Editor requests explicit API release of an existing webhook lock for the supplied scope.

## Outcome

The lock is removed and the response reports success and Lock released.

## Edge cases

- If no lock exists, release still reports success and performs no retained removal. An existing non-webhook lock takes the refusal cases.
