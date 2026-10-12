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
      "text": "The locale option changes the eligible address set using the inspected sitemap rules.",
      "entities": [
        {
          "entity": "page",
          "effect": "reads",
          "facts": [
            "Host",
            "Slug",
            "Locale",
            "Translations",
            "Publication date",
            "Robots",
            "Variant master"
          ]
        }
      ],
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

# Read site content — sitemap locale

## Trigger

Read site content through public website using the sitemap locale way.

## Outcome

The locale option changes the eligible address set using the inspected sitemap rules.
