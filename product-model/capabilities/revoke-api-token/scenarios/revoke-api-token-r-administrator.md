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
      "text": "Clear the credential candidate and save the profile.",
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
      "text": "The token-revocation request receives its stronger-context refusal outcome.",
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
    }
  ]
}
---

# Revoke api token — administrator

## Trigger

Revoke api token through editorial administration using the administrator way.

## Outcome

The token-revocation request receives its stronger-context refusal outcome.
