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
      "text": "Request selected-content output generation.",
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
      "text": "The selected content generation follows supported entry checks and downstream selection, and can also produce its own feed.",
      "entities": [
        {
          "entity": "static-generation",
          "effect": "creates",
          "facts": [
            "Scope",
            "Status",
            "Output",
            "Errors"
          ]
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
      "target": "packages/static-generator/src/Controller/Api/StaticApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/StaticCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/Generator/PageGenerator.php"
    }
  ]
}
---

# Generate static page — selected generation

## Trigger

No prior retained information exists for the selected scope. Generate static page through operator CLI using the selected generation way.

## Outcome

The selected content generation follows supported entry checks and downstream selection, and can also produce its own feed.

This selected pass does not advance Last full generation.
