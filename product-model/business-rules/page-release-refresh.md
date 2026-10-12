---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "release-page-updates",
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
      "target": "packages/admin/src/Controller/PageCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/PageApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Service/PageFrontmatterMapper.php"
    }
  ]
}
---

# Releasing a hold allows subsequent refresh

Clearing a hold allows applicable subsequent output refresh and may queue refresh through the inspected release path. No deadline, successful dispatch or deployed delivery is implied.
