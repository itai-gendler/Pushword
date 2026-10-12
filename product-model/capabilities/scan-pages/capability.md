---
{
  "availability": [
    {
      "place": "administration::editorial"
    },
    {
      "place": "cms-api::editorial"
    },
    {
      "place": "operator-cli"
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

# Scan pages

Run or reuse a Page scan and retain observable status, output and findings for its scope.
