---
{
  "kind": "edge",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "administrator",
      "text": "Request checking for the selected content scope.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::page-scan"
        }
      }
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "Dispatch failure is reported as an observable error.",
      "entities": [
        {
          "entity": "page-scan",
          "effect": "changes",
          "facts": [
            "Scope",
            "Status",
            "Output"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::page-scan"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/page-scanner/src/Controller/PageScannerController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/page-scanner/src/Controller/Api/PageScanApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/page-scanner/src/Command/PageScannerCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/page-scanner/src/Service/PageScanCoordinator.php"
    }
  ]
}
---

# Scan pages — dispatch failure

## Trigger

A selected scope has retained process information, no blocking run, and a new background dispatch throws an exception. Scan pages through editorial administration using the dispatch failure way.

## Outcome

The scope output records the failure message and Status becomes error. Dispatch failure is reported as an observable error.
