---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "delete-page",
      "contexts": [
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

Soft deletion always retains the source as a redirect-only record to the supplied destination, with publication cleared. Redirect fallback can still emit its destination, so draft status is not universal redirect suppression.
