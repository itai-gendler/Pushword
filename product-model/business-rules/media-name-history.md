---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "image",
      "facts": [
        "Filename",
        "Filename history"
      ]
    },
    {
      "type": "entity",
      "id": "file",
      "facts": [
        "Filename",
        "Filename history"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Entity/Media.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/EventListener/MediaLicenseSeedListener.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/EventListener/MediaLicenseStateListener.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/EventListener/MediaNamingListener.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/MediaApiController.php"
    }
  ]
}
---

# Media renames preserve supported historical lookup

Supported rename paths check their applicable naming conflicts and maintain storage/name history. The API can explicitly replace naming history. Storage deletion and rename are not asserted atomic.
