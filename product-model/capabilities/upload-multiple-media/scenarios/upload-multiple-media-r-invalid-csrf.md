---
{
  "kind": "validation",
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
      "text": "Invalid upload proof creates no media.",
      "entities": [],
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

# Upload multiple media — invalid csrf

## Trigger

Upload multiple media through editorial administration using the invalid csrf way.

## Outcome

Invalid upload proof creates no media.
