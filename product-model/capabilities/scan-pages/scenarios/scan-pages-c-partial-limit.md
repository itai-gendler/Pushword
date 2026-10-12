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
      "text": "The selected scan limit reports a partial processed scope rather than establishing that all content was checked.",
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

# Scan pages — partial limit

## Trigger

Scan pages through operator CLI using the partial limit way.

## Outcome

The selected scan limit reports a partial processed scope rather than establishing that all content was checked.
