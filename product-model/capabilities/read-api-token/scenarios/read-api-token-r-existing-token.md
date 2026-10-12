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
      "text": "Request the already retained credential.",
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
      "text": "The already retained token is returned through this supported read path without generation.",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "API token"
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
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Command/UserTokenCommand.php"
    }
  ]
}
---

# Read api token — existing token

## Trigger

Read api token through editorial administration using the existing token way.

## Outcome

The already retained token is returned through this supported read path without generation.
