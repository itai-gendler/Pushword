---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "changes",
      "contexts": [
        {
          "place": "administration::account"
        }
      ],
      "facts": [
        "Password",
        "Password change required"
      ]
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "uses",
          "entity": "user"
        }
      ],
      "when": [
        {
          "fact": "Password change required",
          "is": true
        }
      ]
    },
    {
      "related": [
        {
          "verb": "uses",
          "entity": "editor"
        }
      ],
      "when": [
        {
          "fact": "Password change required",
          "is": true
        }
      ]
    },
    {
      "related": [
        {
          "verb": "uses",
          "entity": "administrator"
        }
      ],
      "when": [
        {
          "fact": "Password change required",
          "is": true
        }
      ]
    },
    {
      "related": [
        {
          "verb": "uses",
          "entity": "super-administrator"
        }
      ],
      "when": [
        {
          "fact": "Password change required",
          "is": true
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/UserController.php"
    }
  ]
}
---

# The related account holder completes required password changes

Own required-password completion changes only the credential and required-change flag.
