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
      "text": "An absent usable index is handled by the inspected empty-result path rather than returning unindexed content. JSON returns empty results without a homepage lookup; the HTML response uses an existing homepage for its surrounding rendering.",
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

# Search site — absent index

## Trigger

Search site through public website using the absent index way.

## Outcome

An absent usable index is handled by the inspected empty-result path rather than returning unindexed content. JSON returns empty results without a homepage lookup; the HTML response uses an existing homepage for its surrounding rendering.
