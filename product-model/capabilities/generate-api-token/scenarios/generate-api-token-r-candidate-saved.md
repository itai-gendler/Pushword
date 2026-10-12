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
      "text": "Generate the credential candidate and save the profile.",
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
      "text": "The generated token candidate becomes the retained API credential only when the profile form is saved.",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "API token"
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
    }
  ]
}
---

# Generate api token — candidate saved

## Trigger

Generate api token through editorial administration using the candidate saved way.

## Outcome

The generated token candidate becomes the retained API credential only when the profile form is saved.
