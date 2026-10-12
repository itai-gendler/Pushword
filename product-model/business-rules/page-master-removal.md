---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "delete-page",
      "contexts": [
        {
          "place": "administration::editorial"
        },
        {
          "place": "cms-api::editorial"
        },
        {
          "place": "operator-cli"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Service/VariantManager.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Entity/Page.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/EventListener/PageListener.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Repository/PageRepository.php"
    }
  ]
}
---

# Removing a master can promote a found replacement

Removing a master can promote a found replacement and reassign applicable links. The inspected candidate selection establishes no deterministic replacement priority.
