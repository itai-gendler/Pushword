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
      "text": "Request removal of the selected profile.",
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
      "text": "The selected CMS profile is removed; referenced-record deletion consequences are not fully established.",
      "entities": [
        {
          "entity": "account",
          "effect": "removes"
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
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Command/UserDeleteCommand.php"
    }
  ]
}
---

# Delete user — account

## Trigger

Delete user through editorial administration using the account way.

## Outcome

The selected CMS profile is removed; referenced-record deletion consequences are not fully established.
