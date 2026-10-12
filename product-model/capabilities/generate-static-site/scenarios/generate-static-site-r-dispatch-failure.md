---
{
  "kind": "edge",
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
      "text": "Dispatch failure leaves an observable error outcome instead of an accepted-running claim.",
      "entities": [
        {
          "entity": "static-generation",
          "effect": "changes",
          "facts": [
            "Scope",
            "Status",
            "Output"
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
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/StaticGenerationCoordinator.php"
    }
  ]
}
---

# Generate static site — dispatch failure

## Trigger

A selected scope has retained process information, no blocking run, and a new background dispatch throws an exception. Generate static site through editorial administration using the dispatch failure way.

## Outcome

The scope output records the failure message and Status becomes error. Dispatch failure leaves an observable error outcome instead of an accepted-running claim.
