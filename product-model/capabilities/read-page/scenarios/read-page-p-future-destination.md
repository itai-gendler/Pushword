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
      "text": "Fallback can redirect to a destination whose content is not yet publicly resolvable.",
      "entities": [
        {
          "entity": "redirection",
          "effect": "reads",
          "facts": [
            "Slug",
            "Destination",
            "Response code"
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

# Read page — future destination

## Trigger

Read page through public website using the future destination way.

## Outcome

Fallback can redirect to a destination whose content is not yet publicly resolvable.
