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
      "text": "The addressed content and its rendered public facts are returned when the applicable resolution predicates pass.",
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

# Read page — page

## Trigger

Read page through signed-in website using the page way.

## Outcome

The addressed content and its rendered public facts are returned when the applicable resolution predicates pass.
