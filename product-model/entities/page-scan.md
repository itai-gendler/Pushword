---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/page-scanner/src/Controller/Api/PageScanApiController.php"
    }
  ]
}
---

# Page scan

The latest retained scan status, output and findings for a scope.

## Information kept

- **Scope** — The retained operation scope or normalized lock key.
- **Status** — The latest reported processing state; it is not a delivery guarantee.
- **Output** — The latest retained processing output for the addressed scope.
- **Result timestamp** — The retained time of the latest scan result used by interval/cache coordination.
- **Findings** — The retained aggregated checker results for the selected scan.
- **Error count** — The retained aggregated scan error count.
