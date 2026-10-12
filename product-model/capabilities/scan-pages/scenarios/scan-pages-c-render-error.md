---
{
  "kind": "edge",
  "routes": {
    "main": "Operator CLI"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "site-operator",
      "text": "Request checking for the selected content scope.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "operator-cli"
        }
      }
    },
    {
      "kind": "product",
      "actor": "site-operator",
      "text": "Rendering failures contribute supported error findings.",
      "entities": [
        {
          "entity": "page-scan",
          "effect": "changes",
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
          "place": "operator-cli"
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

# Scan pages — render error

## Trigger

Scan pages through operator CLI using the render error way.

## Outcome

Rendering failures contribute supported error findings.
