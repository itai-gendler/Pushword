---
{
  "kind": "validation",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "administrator",
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
      "actor": "administrator",
      "text": "The credential-read request receives its stronger-context refusal outcome.",
      "entities": [],
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

# Read api token — administrator

## Trigger

Read api token through editorial administration using the administrator way.

## Outcome

The credential-read request receives its stronger-context refusal outcome.
