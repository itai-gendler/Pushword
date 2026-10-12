---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "page",
      "effect": "changes",
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

# Only Administrator, Super Administrator may change Page

Historical browsing, comparison and comparison writes use the stronger version-administration role checks.
