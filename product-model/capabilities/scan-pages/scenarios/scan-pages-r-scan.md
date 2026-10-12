---
{
  "kind": "primary",
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
      "text": "The selected scope is scanned and retains its latest output/result findings.",
      "entities": [
        {
          "entity": "page-scan",
          "effect": "creates",
          "facts": [
            "Scope",
            "Status",
            "Output",
            "Result timestamp",
            "Findings",
            "Error count"
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
    }
  ]
}
---

# Scan pages — scan

## Trigger

No prior retained information exists for the selected scope. Scan pages through editorial administration using the scan way.

## Outcome

The selected scope is scanned and retains its latest output/result findings.
