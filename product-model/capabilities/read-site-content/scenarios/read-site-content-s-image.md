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
      "text": "The addressed raster original or supported media response is returned.",
      "entities": [
        {
          "entity": "image",
          "effect": "reads",
          "facts": [
            "Stored file",
            "Filename",
            "MIME type"
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

# Read site content — image

## Trigger

Read site content through signed-in website using the image way.

## Outcome

The addressed raster original or supported media response is returned.
