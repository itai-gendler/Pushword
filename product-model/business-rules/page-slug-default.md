---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "create-content",
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
      "id": "import-pages",
      "contexts": [
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
    }
  ]
}
---

# Empty ordinary Page slugs receive an eight-character fallback

An empty ordinary Page slug receives the listener’s eight-character fallback. This is not universal title-derived addressing and no retry guarantee for fallback collision is established.
