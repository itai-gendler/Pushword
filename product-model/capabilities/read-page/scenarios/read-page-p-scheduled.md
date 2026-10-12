---
{
  "kind": "validation",
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
      "text": "Future publication excludes ordinary content until the date is due; redirect fallback is a separate path.",
      "entities": [],
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

# Read page — scheduled

## Trigger

Read page through public website using the scheduled way.

## Outcome

Future publication excludes ordinary content until the date is due; redirect fallback is a separate path.
