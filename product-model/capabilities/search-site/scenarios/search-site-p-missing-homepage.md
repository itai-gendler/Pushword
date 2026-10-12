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
      "text": "Without a homepage the HTML search response is not found. JSON search returns before this lookup and does not require a homepage.",
      "entities": [],
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

# Search site — missing homepage

## Trigger

Search site through public website using the missing homepage way.

## Outcome

Without a homepage the HTML search response is not found. JSON search returns before this lookup and does not require a homepage.
