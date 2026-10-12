---
{
  "kind": "edge",
  "routes": {
    "main": "Operator CLI"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "site-operator",
      "text": "Submit the new profile and credential input.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "operator-cli"
        }
      }
    },
    {
      "kind": "product",
      "actor": "site-operator",
      "text": "The operator-created profile can retain required password completion, masking ordinary effective roles.",
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
          "place": "operator-cli"
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

# Create user — forced password change

## Trigger

Create user through operator CLI using the forced password change way.

## Outcome

The operator-created profile can retain required password completion, masking ordinary effective roles.
