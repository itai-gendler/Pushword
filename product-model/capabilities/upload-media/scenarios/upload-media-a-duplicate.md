---
{
  "kind": "edge",
  "routes": {
    "main": "CMS API"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Upload raster content whose hash already belongs to a retained asset, with different submitted metadata.",
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
      "text": "An identical content hash returns existing media before new submitted metadata is applied.",
      "entities": [
        {
          "entity": "image",
          "effect": "reads",
          "facts": [
            "Filename",
            "MIME type",
            "Size",
            "Content hash",
            "Filename history",
            "Alternative text",
            "Localized text",
            "Tags",
            "Custom properties",
            "Licensing origin",
            "Dimensions",
            "Color information"
          ]
        }
      ],
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
      "target": "packages/api/src/Controller/MediaApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/MediaCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/EventListener/MediaLicenseSeedListener.php"
    }
  ]
}
---

# Upload media — duplicate

## Trigger

Upload media through editorial API using the duplicate way.

## Outcome

An identical content hash returns existing media before new submitted metadata is applied.
