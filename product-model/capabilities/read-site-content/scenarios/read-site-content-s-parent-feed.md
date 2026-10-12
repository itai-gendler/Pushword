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
      "text": "Request the selected public resource.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "website::signed-in"
        }
      }
    },
    {
      "kind": "product",
      "actor": "user",
      "text": "The selected parent’s eligible children determine its feed.",
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
            "Locale",
            "Publication date",
            "Robots",
            "Parent"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "website::signed-in"
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

# Read site content — parent feed

## Trigger

Read site content through signed-in website using the parent feed way.

## Outcome

The selected parent’s eligible children determine its feed.
