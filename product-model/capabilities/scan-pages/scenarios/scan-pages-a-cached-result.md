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
      "text": "Request checking for the selected content scope.",
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
      "text": "A recent retained result can be reused under interval/force coordination.",
      "entities": [
        {
          "entity": "page-scan",
          "effect": "reads",
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
          "place": "cms-api::editorial"
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

# Scan Pages — cached result

## Trigger

An Editor requests a scan through the API without Force, with no blocking scan and a retained result inside the configured minimum interval.

## Outcome

The response reports started false and returns the current cached findings and scope status. No new scan is dispatched or retained result written by this request.
