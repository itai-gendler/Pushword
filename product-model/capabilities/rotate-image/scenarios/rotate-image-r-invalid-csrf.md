---
{
  "kind": "validation",
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
      "text": "Invalid administration request proof leaves raster content unchanged.",
      "entities": [],
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

# Rotate image — invalid csrf

## Trigger

Rotate image through editorial administration using the invalid csrf way.

## Outcome

Invalid administration request proof leaves raster content unchanged.
