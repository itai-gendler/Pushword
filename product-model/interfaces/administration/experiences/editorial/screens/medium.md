---
{
  "entities": [
    {
      "entity": "image",
      "shows": [
        "Filename",
        "Filename history",
        "Alternative text",
        "Localized text",
        "Tags",
        "Custom properties",
        "Rights values",
        "Licensing origin"
      ],
      "collects": [
        "Stored file",
        "Filename",
        "Alternative text",
        "Localized text",
        "Tags",
        "Custom properties",
        "Rights values"
      ]
    },
    {
      "entity": "file",
      "shows": [
        "Filename",
        "Filename history",
        "Alternative text",
        "Localized text",
        "Tags",
        "Custom properties",
        "Rights values",
        "Licensing origin"
      ],
      "collects": [
        "Stored file",
        "Filename",
        "Alternative text",
        "Localized text",
        "Tags",
        "Custom properties",
        "Rights values"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/MediaCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/DependencyInjection/Configuration.php"
    }
  ]
}
---

# Medium

The selected asset’s supported descriptive, naming, replacement and rights inputs, with raster-specific rotation where applicable.
