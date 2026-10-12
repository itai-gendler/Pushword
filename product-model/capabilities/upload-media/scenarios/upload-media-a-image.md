---
{
  "kind": "primary",
  "routes": {
    "main": "CMS API"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Supply the selected upload and descriptive input.",
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
      "text": "An accepted raster upload creates independently addressed media with retained descriptive/storage values.",
      "entities": [
        {
          "entity": "image",
          "effect": "creates",
          "facts": [
            "Reference",
            "Filename",
            "Filename history",
            "Stored file",
            "MIME type",
            "Size",
            "Content hash",
            "Original hash",
            "Alternative text",
            "Localized text",
            "Tags",
            "Inherited tags",
            "Hidden from administration",
            "Custom properties",
            "Created at",
            "Updated at",
            "Dimensions",
            "Color information",
            "Rights values",
            "Licensing origin"
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

# Upload media — image

## Trigger

Upload media through editorial API using the image way.

## Outcome

An accepted raster upload creates independently addressed media with retained descriptive/storage values.
