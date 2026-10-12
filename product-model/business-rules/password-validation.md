---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "reset-password",
      "contexts": [
        {
          "place": "administration::login"
        }
      ]
    },
    {
      "type": "capability",
      "id": "change-password",
      "contexts": [
        {
          "place": "administration::account"
        },
        {
          "place": "administration::login"
        }
      ]
    },
    {
      "type": "capability",
      "id": "create-user",
      "contexts": [
        {
          "place": "administration::editorial"
        },
        {
          "place": "operator-cli"
        }
      ]
    },
    {
      "type": "capability",
      "id": "edit-user",
      "contexts": [
        {
          "place": "administration::editorial"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/UserController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Entity/User.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Service/MagicLinkMailer.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Command/UserCreateCommand.php"
    }
  ]
}
---

# Credential validation follows its handler

Link/required-change handlers require at least seven characters and matching confirmation; they do not establish the profile form’s maximum-one-hundred constraint. Administration profile validation has its own checks. The operator creation command hashes supplied credentials without invoking the same form validator.
