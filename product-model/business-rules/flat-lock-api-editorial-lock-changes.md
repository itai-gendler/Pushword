---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "editorial-lock",
      "effect": "changes",
      "contexts": [
        {
          "place": "cms-api::editorial"
        }
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "editor"
      ]
    },
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
      "target": "packages/flat/src/Controller/FlatLockApiController.php"
    }
  ]
}
---

# Only Editor, Administrator, Super Administrator may change Editorial lock

The supported lock API checks effective editorial privilege. Explicit release of an existing lock requires webhook kind, without owner-only release.
