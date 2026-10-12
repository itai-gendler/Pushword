---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "static-generation",
      "effect": "reads",
      "contexts": [
        {
          "place": "administration::editorial"
        }
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "administrator"
      ]
    },
    {
      "actors": [
        "super-administrator"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/StaticController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/page-scanner/src/Controller/PageScannerController.php"
    }
  ]
}
---

# Only Administrator, Super Administrator may read Static generation

Generation and scanning use this entry contract’s role or operator authority; retained status does not establish successful output.
