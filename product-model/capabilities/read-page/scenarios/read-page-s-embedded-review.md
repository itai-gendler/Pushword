---
{
  "kind": "primary",
  "routes": {
    "main": "Signed-in website"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "user",
      "text": "Open the selected content address.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "website::signed-in::page"
        }
      }
    },
    {
      "kind": "product",
      "actor": "user",
      "text": "Rendered content includes matching published reviews and their applicable rating, reply and locale values.",
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
          "entity": "review",
          "effect": "reads",
          "facts": [
            "Title",
            "Content",
            "Rating",
            "Reply",
            "Reply author",
            "Localized title/content"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "website::signed-in::page"
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

# Read page — embedded review

## Trigger

Read page through signed-in website using the embedded review way.

## Outcome

Rendered content includes matching published reviews and their applicable rating, reply and locale values.
