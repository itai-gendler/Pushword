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
      "text": "Request the profile collection.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::users"
        }
      }
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "The profile collection request receives its stronger-context refusal outcome.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::users"
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

# Browse users — administrator

## Trigger

Browse users through editorial administration using the administrator way.

## Outcome

The account collection request receives its stronger-context refusal outcome.
