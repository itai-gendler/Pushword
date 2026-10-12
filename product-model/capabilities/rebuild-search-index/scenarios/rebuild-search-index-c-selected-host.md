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
      "text": "The selected configured host’s full search projection is rebuilt from the eligible content set.",
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

# Rebuild search index — selected host

## Trigger

Rebuild search index through operator CLI using the selected host way.

## Outcome

The selected site’s full search projection is rebuilt from the eligible content set.
