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
      "text": "Submit the selected changes through the specified edit path.",
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
      "text": "The accepted image name change updates naming history and moves the stored master and applicable derivatives through the storage listener.",
      "entities": [
        {
          "entity": "image",
          "effect": "changes",
          "facts": [
            "Filename",
            "Filename history",
            "Stored file"
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
      "target": "packages/core/src/EventListener/MediaNamingListener.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/EventListener/MediaStorageListener.php"
    }
  ]
}
---

# Edit content — media rename

## Trigger

An Editor updates an existing raster image through the media API with a different valid filename that does not collide with another retained name or history.

## Outcome

The filename and naming history are updated. The master and applicable derivatives follow the inspected storage move; an exception does not establish an atomic operation. This endpoint has no Page revision requirement.
