---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "generate-static-site",
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

# Incomplete site replacement can preserve prior output

A full run with no eligible published Pages or without the required generated index can preserve previous site output rather than universally erase it. Unpublishing content therefore does not itself guarantee that all served static output disappears.
