---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "removes",
      "contexts": [
        {
          "place": "administration::editorial::users"
        },
        {
          "place": "administration::editorial::user"
        }
      ]
    }
  ],
  "permits": [
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
      "target": "packages/admin/src/Controller/UserCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Resources/config/packages/security.php"
    }
  ]
}
---

# Only Super Administrator may remove Account

The shipped account-management role governs profile administration; required password completion masks its ordinary privilege.
