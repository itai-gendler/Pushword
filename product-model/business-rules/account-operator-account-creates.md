---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "creates",
      "contexts": [
        {
          "place": "operator-cli"
        }
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "site-operator"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Command/UserCreateCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Command/UserDeleteCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Command/UserTokenCommand.php"
    }
  ]
}
---

# Only Site Operator may create Account

The deployment-level account commands support existing-credential reading, profile creation and removal without CMS sign-in.
