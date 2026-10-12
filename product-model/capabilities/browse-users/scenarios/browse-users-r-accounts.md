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
      "actor": "super-administrator",
      "text": "The collection discloses supported profile, role and creation facts without stored passwords.",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Reference",
            "Email",
            "Username",
            "Interface locale",
            "Roles",
            "Created at"
          ]
        }
      ],
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

# Browse users — accounts

## Trigger

Browse users through editorial administration using the accounts way.

## Outcome

The collection discloses supported profile, role and creation facts without stored passwords.
