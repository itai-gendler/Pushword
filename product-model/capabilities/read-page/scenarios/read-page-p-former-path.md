---
{
  "kind": "edge",
  "routes": {
    "main": "Public website"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "visitor",
      "text": "Open the selected content address.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "website::public::page"
        }
      }
    },
    {
      "kind": "product",
      "actor": "visitor",
      "text": "The old source path resolves to its retained destination unless a real stored path occupies that address.",
      "entities": [
        {
          "entity": "page-redirect",
          "effect": "reads",
          "facts": [
            "Source path",
            "Response code"
          ]
        },
        {
          "entity": "page",
          "effect": "reads",
          "facts": [
            "Slug",
            "Host"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "website::public::page"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/PageResolver.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/PageController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Repository/PageRepository.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/PageApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Entity/Review.php"
    }
  ]
}
---

# Read page — former path

## Trigger

Read page through public website using the former path way.

## Outcome

The old source path resolves to its retained destination unless a real stored path occupies that address.
