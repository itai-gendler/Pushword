---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "static-generation",
      "effect": "changes",
      "contexts": [
        {
          "place": "operator-cli"
        }
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "site-operator"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/StaticCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/page-scanner/src/Command/PageScannerCommand.php"
    }
  ]
}
---

# Only Site Operator may change Static generation

Generation and scanning use this entry contract’s role or operator authority; retained status does not establish successful output.
