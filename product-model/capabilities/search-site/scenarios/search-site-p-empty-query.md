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
      "text": "An empty query does not invent matching content. JSON returns empty results without a homepage lookup; the HTML response uses an existing homepage for its surrounding rendering.",
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

# Search site — empty query

## Trigger

Search site through public website using the empty query way.

## Outcome

An empty query does not invent matching content. JSON returns empty results without a homepage lookup; the HTML response uses an existing homepage for its surrounding rendering.
