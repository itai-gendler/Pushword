---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "file",
      "effect": "removes",
      "contexts": [
        {
          "place": "administration::editorial::multiple-upload"
        }
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "administrator"
      ]
    },
    {
      "actors": [
        "super-administrator"
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

# Only Administrator, Super Administrator may remove File

The multiple-upload process, its inline metadata and its removal operations have the stronger administration guard.
