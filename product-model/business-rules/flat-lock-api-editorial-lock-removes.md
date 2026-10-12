---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "editorial-lock",
      "effect": "removes",
      "contexts": [
        {
          "place": "cms-api::editorial"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Controller/FlatLockApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Service/FlatApiTokenValidator.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Service/FlatLockManager.php"
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
  ]
}
---

# Editorial API processing removes locks for editorial roles

API processing requires the authenticated account’s effective editorial authority. Explicit webhook release and expiry cleanup during status checking retain their distinct operation constraints. Removal is not restricted to the identity recorded when the lock was acquired.
