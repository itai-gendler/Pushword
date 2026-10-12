---
{
  "kind": "primary",
  "result": "achieved",
  "routes": {
    "main": "Product hand-off"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "user",
      "text": "Supply the selected access method’s input.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::login::sign-in"
        }
      },
      "capability": "sign-in"
    },
    {
      "kind": "product",
      "actor": "user",
      "text": "The own-profile email access request sends the setup link and carries password completion into its separate run.",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Email",
            "Roles",
            "Password change required"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::login::sign-in"
        }
      },
      "capability": "sign-in"
    },
    {
      "kind": "product",
      "actor": "user",
      "capability": "sign-in",
      "text": "The Product’s own-request setup email carries the person to credential completion.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::login::sign-in"
        }
      }
    },
    {
      "kind": "actor",
      "actor": "user",
      "text": "Submit the replacement credential and confirmation.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::login::password"
        }
      },
      "capability": "change-password"
    },
    {
      "kind": "product",
      "actor": "user",
      "text": "A valid setup-purpose link completes the bound profile’s password setup; the forgot-password request setting is not imposed on this link handler.",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Password",
            "Password change required"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::login::password"
        }
      },
      "capability": "change-password"
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
      "target": "packages/core/src/Security/LoginFormAuthenticator.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Security/MagicLinkAuthenticator.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Security/OAuthAuthenticator.php"
    }
  ]
}
---

# Complete emailed password setup — setup link

## Trigger

Complete the setup link produced by the own sign-in request.

## Outcome

The bound profile’s replacement credential is accepted through the supplied setup link.
