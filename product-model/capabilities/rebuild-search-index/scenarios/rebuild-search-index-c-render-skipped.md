---
{
  "kind": "edge",
  "routes": {
    "main": "Operator CLI"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "site-operator",
      "text": "Request rebuilding of the selected search projection.",
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
      "text": "Content that fails rendering is skipped rather than indexed as successfully rendered.",
      "entities": [],
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
      "target": "packages/search/src/Command/IndexCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/search/src/Service/IndexManager.php"
    }
  ]
}
---

# Rebuild search index — render skipped

## Trigger

Rebuild search index through operator CLI using the render skipped way.

## Outcome

Content that fails rendering is skipped rather than indexed as successfully rendered.
