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
      "id": "reset-password",
      "contexts": [
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
    }
  ]
}
---

# Email access requests do not disclose unknown profiles

The inspected email access/reset request response does not disclose whether an unknown address has a matching profile; no access link is sent for an absent subject.
