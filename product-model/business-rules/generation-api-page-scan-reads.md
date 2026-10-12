---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "page-scan",
      "effect": "reads",
      "contexts": [
        {
          "place": "cms-api::editorial"
        }
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "editor"
      ]
    },
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
      "target": "packages/static-generator/src/Controller/Api/StaticApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/page-scanner/src/Controller/Api/PageScanApiController.php"
    }
  ]
}
---

# Only Editor, Administrator, Super Administrator may read Page scan

Generation and scanning use this entry contract’s role or operator authority; retained status does not establish successful output.
