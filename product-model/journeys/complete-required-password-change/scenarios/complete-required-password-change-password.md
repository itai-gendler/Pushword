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
      "text": "The existing profile is authenticated with required password completion; the Product carries the person to credential replacement.",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Password change required",
            "Roles"
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
      "kind": "actor",
      "actor": "user",
      "text": "Submit the replacement credential and confirmation.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::account::password"
        }
      },
      "capability": "change-password"
    },
    {
      "kind": "product",
      "actor": "user",
      "text": "Confirmed valid replacement stores the credential and clears the required-change flag.",
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
          "place": "administration::account::password"
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

# Complete required password change — password

## Trigger

Complete the password change required by sign-in.

## Outcome

The new credential is retained and the required-change flag no longer masks ordinary privileges.
