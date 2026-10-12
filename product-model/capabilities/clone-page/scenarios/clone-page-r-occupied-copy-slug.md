---
{
  "kind": "edge",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Request a draft copy of the selected content.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::page"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The clone uses the fixed source address plus -copy. With that address already occupied on the same host, the stored address uniqueness constraint prevents another record; this handler supplies no alternate suffix or guaranteed recovery response.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::page"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/PageCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Service/VariantManager.php"
    }
  ]
}
---

# Clone page — occupied copy slug

## Trigger

Clone page through editorial administration using the occupied copy slug way.

## Outcome

The clone uses the fixed source address plus -copy. With that address already occupied on the same host, the stored address uniqueness constraint prevents another record; this handler supplies no alternate suffix or guaranteed recovery response.
