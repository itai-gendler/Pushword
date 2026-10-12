---
{
  "entities": [
    {
      "entity": "image",
      "shows": [
        "Filename",
        "Alternative text",
        "Tags",
        "Rights values",
        "Licensing origin"
      ],
      "collects": [
        "Stored file",
        "Alternative text",
        "Localized text",
        "Tags",
        "Filename",
        "Rights values"
      ]
    },
    {
      "entity": "file",
      "shows": [
        "Filename",
        "Alternative text",
        "Tags",
        "Rights values",
        "Licensing origin"
      ],
      "collects": [
        "Stored file",
        "Alternative text",
        "Tags",
        "Filename",
        "Rights values"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/MediaMultiUploadController.php"
    }
  ]
}
---

# Multiple upload

The batch upload process showing per-asset outcomes and accepting its supported inline descriptive, naming and rights changes.
