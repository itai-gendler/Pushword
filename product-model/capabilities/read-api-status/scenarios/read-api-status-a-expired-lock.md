---
{
  "kind": "edge",
  "routes": {
    "main": "CMS API"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Request the selected retained status.",
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
      "text": "The Product inspects the retained lock and its expiry inputs.",
      "entities": [
        {
          "entity": "editorial-lock",
          "effect": "reads",
          "facts": [
            "Scope",
            "Kind",
            "Acquired at",
            "TTL"
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
      "text": "Status lookup removes an expired lock and reports the resulting unlocked scope.",
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
      "target": "packages/api/src/Controller/WhoAmIApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Controller/FlatLockApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/Controller/Api/StaticApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/page-scanner/src/Controller/Api/PageScanApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Service/FlatLockManager.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Service/FlatApiTokenValidator.php"
    }
  ]
}
---

# Read API status — expired lock

## Trigger

An Editor requests status for a scope with an existing lock of any kind whose Acquired at plus TTL is strictly earlier than the request’s clock.

## Outcome

Status lookup removes the expired lock and reports unlocked, no lock information and zero remaining seconds. Passing time alone did not delete it; this authenticated request performs the cleanup.
