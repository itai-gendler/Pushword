---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "search-site",
      "contexts": [
        {
          "place": "website::public"
        },
        {
          "place": "website::signed-in"
        }
      ]
    },
    {
      "type": "capability",
      "id": "rebuild-search-index",
      "contexts": [
        {
          "place": "operator-cli"
        }
      ]
    },
    {
      "type": "capability",
      "id": "edit-content",
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
      "target": "packages/search/src/Service/IndexManager.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/search/src/Command/IndexCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/search/src/Controller/SearchController.php"
    }
  ]
}
---

# Search indexing follows full and incremental selection contracts

Full indexing excludes applicable unpublished/noindex/redirect/error content and variants, while the incremental eligibility path has different variant selection. Render errors are skipped. Eligible writes can queue incremental refresh when enabled/not suppressed; time crossing alone does not guarantee index refresh.
