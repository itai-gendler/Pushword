---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "read-page",
      "contexts": [
        {
          "place": "website::public"
        },
        {
          "place": "website::signed-in"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/PageResolver.php"
    },
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

# Ordinary dynamic Page resolution withholds future-created content

For ordinary dynamic resolution, a Page whose Created at value is later than the current clock is not returned as content, even when publication is due. Editorial preview, authorized by the Page-reading permission Rule, bypasses this eligibility condition. No creation-time fact is changed when time passes. Failure to resolve content still allows the controller’s separate redirect fallback. This constraint does not govern static rendering.
