---
{
  "kind": "edge",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Supply the selected upload and descriptive input.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::medium"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "An eligible raster upload without imported rights receives the inspected rights seed.",
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
          "place": "administration::editorial::medium"
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

# Upload media — seeded rights

## Trigger

Upload media through editorial administration using the seeded rights way.

## Outcome

An eligible raster upload without imported rights receives the inspected rights seed.
