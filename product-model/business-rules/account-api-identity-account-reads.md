---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "reads",
      "contexts": [
        {
          "place": "cms-api::editorial"
        }
      ],
      "facts": [
        "Reference",
        "Email",
        "Roles"
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "editor"
      ]
    },
    {
      "actors": [
        "administrator"
      ]
    },
    {
      "actors": [
        "super-administrator"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/WhoAmIApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Security/ApiTokenAuthenticator.php"
    }
  ]
}
---

# Only Editor, Administrator, Super Administrator may read Account

The token-identified profile’s reference, email and effective roles are disclosed. The payload username carries the email identifier. Credential lookup is request identity proof.
