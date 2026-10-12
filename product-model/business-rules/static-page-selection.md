---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "generate-static-page",
      "contexts": [
        {
          "place": "cms-api::editorial"
        },
        {
          "place": "operator-cli"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/StaticAppGenerator.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/Controller/Api/StaticApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/Generator/PageGenerator.php"
    }
  ]
}
---

# Selected generation preserves entry checks and downstream pattern selection

The API performs exact-address prechecks before downstream slug LIKE matching. Pattern characters, including underscore, can select additional records downstream. Selected Page generation can also produce that Page’s own feed. API hold/publication/redirect/cache/error/running checks do not establish operator parity.
