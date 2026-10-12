---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "hold-page-updates",
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
      "id": "release-page-updates",
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
    },
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

# Non-null holds suppress applicable generation

Every non-null hold activates the applicable generation suppression. A hold is not a scheduled release appointment, a separate pending Page or a universal freeze of content, metadata, indexing or dynamic reading.
