---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "delete-page",
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
      "target": "packages/api/src/Controller/PageApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Service/PageFrontmatterMapper.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Entity/Page.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/EventListener/PageListener.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Repository/PageRepository.php"
    }
  ]
}
---

# Soft deletion retains an unpublished redirect-only record

Soft deletion retains a redirect-only source record with publication cleared. Redirect fallback can still emit its destination, so draft status is not universal redirect suppression.
