---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "page-version",
      "effect": "removes",
      "contexts": [
        {
          "place": "administration::editorial::versions"
        },
        {
          "place": "administration::editorial::comparison"
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
      "target": "packages/version/src/VersionController.php"
    }
  ]
}
---

# Only Administrator, Super Administrator may remove Page version

The version collection, comparison, restoration and guarded clearing routes use the stronger administration role.
