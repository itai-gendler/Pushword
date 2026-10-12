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
      "text": "Supply the search query.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "website::signed-in::search"
        }
      }
    },
    {
      "kind": "product",
      "actor": "user",
      "text": "The supplied query yields the supported indexed title, address and excerpt results.",
      "entities": [
        {
          "entity": "page",
          "effect": "reads",
          "facts": [
            "Host",
            "Slug",
            "Heading",
            "Title",
            "Content",
            "Locale"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "website::signed-in::search"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/search/src/Controller/SearchController.php"
    }
  ]
}
---

# Search site — search

## Trigger

Search site through signed-in website using the search way.

## Outcome

The supplied query yields the supported indexed title, address and excerpt results.
