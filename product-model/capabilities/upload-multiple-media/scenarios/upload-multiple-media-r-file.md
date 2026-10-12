---
{
  "kind": "primary",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "administrator",
      "text": "Submit the selected upload batch.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::multiple-upload"
        }
      }
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "The accepted non-raster file creates media and is reported in the per-file uploader result.",
      "entities": [
        {
          "entity": "file",
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
            "Rights values",
            "Licensing origin"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::multiple-upload"
        }
      }
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

# Upload multiple media — file

## Trigger

Upload multiple media through editorial administration using the file way.

## Outcome

The accepted non-raster file creates media and is reported in the per-file uploader result.
