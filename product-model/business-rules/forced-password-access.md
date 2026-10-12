---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "sign-in",
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
      "target": "packages/core/src/Resources/config/packages/security.php"
    }
  ]
}
---

# Required password completion masks ordinary effective roles

A retained required-password flag replaces ordinary effective account roles with the required-change role until completion. Successful authentication alone therefore does not restore editorial privilege. The flag is shared profile information, not another Actor role.
