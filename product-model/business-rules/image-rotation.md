---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "rotate-image",
      "contexts": [
        {
          "place": "administration::editorial"
        },
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
      "target": "packages/admin/src/Controller/MediaCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/MediaApiController.php"
    }
  ]
}
---

# Rotation follows its entry path’s angle and no-op contract

Administration supports its inspected quarter-turn choices and no-op redirect for a non-raster subject; the API accepts its multiple-of-90 contract and full-turn no-op. Applicable raster caches/derived information are refreshed without applying ordinary upload rights seeding.
