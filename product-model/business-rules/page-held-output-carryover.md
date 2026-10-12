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

# Held output carries only existing files at the current slug

Carry-over uses the current slug and only existing generated HTML/feed files and supported compressed companions. A new held address has no prior output to retain. A held rename does not automatically move output from the old slug; applicable incremental metadata can still advance.
