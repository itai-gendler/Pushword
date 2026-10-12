---
{
  "kind": "validation",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
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
      "actor": "editor",
      "text": "The administration scan request receives its stronger-context refusal outcome.",
      "entities": [],
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
    }
  ]
}
---

# Scan pages — editor

## Trigger

Scan pages through editorial administration using the editor way.

## Outcome

The administration scan request receives its stronger-context refusal outcome.
