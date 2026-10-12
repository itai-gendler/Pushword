---
{
  "kind": "primary",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "super-administrator",
      "text": "Submit the selected profile changes.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::user"
        }
      }
    },
    {
      "kind": "product",
      "actor": "super-administrator",
      "text": "Accepted profile, locale, role and credential changes are saved.",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Email",
            "Username",
            "Interface locale",
            "Roles",
            "Password",
            "Created at"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::user"
        }
      }
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
      "target": "packages/core/src/Entity/User.php"
    }
  ]
}
---

# Edit user — account

## Trigger

Edit user through editorial administration using the account way.

## Outcome

Accepted profile, locale, role and credential changes are saved.
