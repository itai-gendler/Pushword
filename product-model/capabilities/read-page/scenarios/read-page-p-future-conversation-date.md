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
      "text": "A future conversation publication date still satisfies the embedded public query’s presence check.",
      "entities": [
        {
          "entity": "page",
          "effect": "reads",
          "facts": [
            "Heading",
            "Title",
            "Content",
            "Slug",
            "Locale",
            "Main image",
            "Translations"
          ]
        },
        {
          "entity": "message",
          "effect": "reads",
          "facts": [
            "Content",
            "Author name",
            "Publication date"
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

# Read page — future conversation date

## Trigger

Read page through public website using the future conversation date way.

## Outcome

A future conversation publication date still satisfies the embedded public query’s presence check.
