---
{
  "kind": "primary",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "administrator",
      "text": "Request whole-scope output generation.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::static-generation"
        }
      }
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "Whole-scope generation runs through its supported dispatch or operator path and retains observable output and reported status.",
      "entities": [
        {
          "entity": "static-generation",
          "effect": "creates",
          "facts": [
            "Scope",
            "Status",
            "Output",
            "Errors",
            "Last full generation"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::static-generation"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/StaticController.php"
    },
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
      "target": "packages/static-generator/src/StaticAppGenerator.php"
    }
  ]
}
---

# Generate static site — whole generation

## Trigger

No prior retained information exists for the selected scope. Generate static site through editorial administration using the whole generation way.

## Outcome

Whole-scope generation runs through its supported dispatch or operator path and retains observable output and reported status.
