---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "scan-pages",
      "contexts": [
        {
          "place": "administration::editorial"
        },
        {
          "place": "cms-api::editorial"
        },
        {
          "place": "operator-cli"
        }
      ]
    },
    {
      "type": "capability",
      "id": "read-api-status",
      "contexts": [
        {
          "place": "cms-api::editorial"
        }
      ]
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
    }
  ]
}
---

# Scans preserve coordination and retained-result outcomes

Observed process coordination includes cross-locking, interval/force policy, retained result reuse, running/queued reporting and dispatch errors. Limits and renderer errors affect reported findings; the checker set is not asserted exhaustive.
