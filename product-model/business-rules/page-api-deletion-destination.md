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

API deletion requires a supported destination and rejects missing or self targets. This holds under both delete strategies; administration and operator deletion do not require a destination.
