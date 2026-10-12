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
      "text": "Host-aware robots text is returned with the configured base address and available locale sitemap addresses.",
      "entities": [
        {
          "entity": "site",
          "effect": "reads",
          "facts": [
            "Host",
            "Locale",
            "Base URL",
            "Rendering settings"
          ]
        },
        {
          "entity": "page",
          "effect": "reads",
          "facts": [
            "Host",
            "Locale"
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
      "target": "packages/core/src/Controller/RobotsTxtController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/templates/page/robots.txt.twig"
    }
  ]
}
---

# Read site content — robots

## Trigger

Read site content through signed-in website using the robots way.

## Outcome

Site-aware robots text is returned with the configured public base address.
