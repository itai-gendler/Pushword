---
{
  "kind": "edge",
  "routes": {
    "main": "Signed-in website"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
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
      "actor": "editor",
      "text": "The Product resolves and renders the selected Draft, Scheduled or future-created Page for this request.",
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

# Read Page — draft preview

## Trigger

An Editor opens the dynamic website address of a Draft Page; the same preview path also handles a Scheduled or future-created Page.

## Outcome

The selected Page is returned and rendered without altering its publication or creation date.
