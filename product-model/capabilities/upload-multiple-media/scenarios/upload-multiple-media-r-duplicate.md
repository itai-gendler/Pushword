---
{
  "kind": "edge",
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
      "text": "Duplicate media is reported as an existing/skipped result, not another newly created record.",
      "entities": [
        {
          "entity": "image",
          "effect": "reads",
          "facts": [
            "Filename",
            "Content hash"
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

# Upload multiple media — duplicate

## Trigger

Upload multiple media through editorial administration using the duplicate way.

## Outcome

Duplicate media is reported as an existing/skipped result, not another newly created record.
