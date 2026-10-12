---
{
  "kind": "primary",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Request the supported rotation.",
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
      "text": "A supported rotation changes raster content and refreshes its applicable derived information/cache.",
      "entities": [
        {
          "entity": "image",
          "effect": "changes",
          "facts": [
            "Stored file",
            "Content hash",
            "Dimensions",
            "Color information",
            "Size"
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
      "target": "packages/admin/src/Controller/MediaCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/MediaApiController.php"
    }
  ]
}
---

# Rotate image — image

## Trigger

Rotate image through editorial administration using the image way.

## Outcome

A supported rotation changes raster content and refreshes its applicable derived information/cache.
