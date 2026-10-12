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
      "text": "The addressed stored file is returned through the public media path.",
      "entities": [
        {
          "entity": "file",
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

# Read site content — file

## Trigger

Read site content through signed-in website using the file way.

## Outcome

The addressed stored file is returned through the public media path.
