---
{
  "kind": "primary",
  "routes": {
    "main": "Operator CLI"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "site-operator",
      "text": "Request the selected deletion strategy with its destination or confirmation.",
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
      "text": "Confirmed operator deletion removes the matching tagged ordinary records.",
      "entities": [
        {
          "entity": "page",
          "effect": "removes",
          "from": "Published"
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
      "target": "packages/api/src/Controller/PageApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Command/DeletePageCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/PageCrudController.php"
    }
  ]
}
---

# Delete page — tagged pages

## Trigger

Delete page through operator CLI using the tagged pages way.

## Outcome

Confirmed operator deletion removes the matching tagged ordinary records.
