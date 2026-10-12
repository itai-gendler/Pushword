---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "delete-page",
      "contexts": [
        {
          "place": "administration::editorial"
        },
        {
          "place": "cms-api::editorial"
        },
        {
          "place": "operator-cli"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/PageApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Service/PageFrontmatterMapper.php"
    }
  ]
}
---

# Page API deletion requires a supported destination

API deletion requires a supported destination and rejects missing or self targets. An existing internal non-redirect destination can receive the old path while the source is removed; other supported destinations retain a redirect record. These strategies do not become ordinary administration or operator deletion parity.
