---
{
  "kind": "validation",
  "routes": {
    "main": "CMS API"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Supply the future publication instant.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "cms-api::editorial"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "Invalid date input does not set a publication date.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "cms-api::editorial"
        }
      }
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

# Schedule page — invalid date

## Trigger

Schedule page through editorial API using the invalid date way.

## Outcome

Invalid date input does not set a publication date.
