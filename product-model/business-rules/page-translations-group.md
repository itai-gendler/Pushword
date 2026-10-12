---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "add-page-translation",
      "contexts": [
        {
          "place": "administration::editorial"
        },
        {
          "place": "cms-api::editorial"
        }
      ]
    },
    {
      "type": "capability",
      "id": "remove-page-translation",
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

# Translation changes preserve reciprocal group effects

Adding/removing translation links has reciprocal/group effects. The API resolves every supplied reference before mutating; registered host/slug references permit cross-host linking. Unknown references abort the intended translation mutation.
