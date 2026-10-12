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
      "text": "Submit the new profile and credential input.",
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
      "text": "Accepted profile and credential input creates the selected CMS profile.",
      "entities": [
        {
          "entity": "account",
          "effect": "creates",
          "facts": [
            "Reference",
            "Email",
            "Username",
            "Interface locale",
            "Roles",
            "Password",
            "API token",
            "Password change required",
            "Created at",
            "Custom properties"
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
      "target": "packages/core/src/Command/UserCreateCommand.php"
    }
  ]
}
---

# Create user — account

## Trigger

Create user through editorial administration using the account way.

## Outcome

Accepted profile and credential input creates the selected CMS profile.
