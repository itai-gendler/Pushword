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
      "actor": "editor",
      "text": "The request receives the stronger uploader’s refusal outcome.",
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

# Upload multiple media — editor

## Trigger

Upload multiple media through editorial administration using the editor way.

## Outcome

The request receives the stronger uploader’s refusal outcome.
