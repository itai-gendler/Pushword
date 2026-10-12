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
      "text": "Request the selected public resource.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "website::public"
        }
      }
    },
    {
      "kind": "product",
      "actor": "visitor",
      "text": "Without the required locale homepage the main feed does not resolve.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "website::public"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/MediaCacheController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/MediaController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/SitemapController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/FeedController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/RobotsTxtController.php"
    }
  ]
}
---

# Read site content — missing feed homepage

## Trigger

Read site content through public website using the missing feed homepage way.

## Outcome

Without the required locale homepage the main feed does not resolve.
