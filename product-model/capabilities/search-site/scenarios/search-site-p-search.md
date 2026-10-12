---
{
  "kind": "primary",
  "routes": {
    "main": "Public website"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "visitor",
      "text": "Supply the search query.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "website::public::search"
        }
      }
    },
    {
      "kind": "product",
      "actor": "visitor",
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
          "place": "website::public::search"
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

Search site through public website using the search way.

## Outcome

The supplied query yields the supported indexed title, address and excerpt results.
