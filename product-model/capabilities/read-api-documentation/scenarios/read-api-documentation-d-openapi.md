---
{
  "kind": "primary",
  "routes": {
    "main": "API documentation"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "visitor",
      "text": "Request the supported API contract document.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "cms-api::documentation"
        }
      }
    },
    {
      "kind": "product",
      "actor": "visitor",
      "text": "The supported documentation document is returned without executing editorial operations.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "cms-api::documentation"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/DocsApiController.php"
    }
  ]
}
---

# Read api documentation — openapi

## Trigger

Read api documentation through API documentation using the openapi way.

## Outcome

The supported documentation document is returned without executing editorial operations.
