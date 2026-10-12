---
{
  "kind": "primary",
  "routes": {
    "main": "CMS API"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Open the selected content address.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "cms-api::editorial"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The selected content is returned as canonical raw frontmatter and body. Draft, scheduled and held values are included; dynamic public-resolution predicates do not filter this editorial read.",
      "entities": [
        {
          "entity": "page",
          "effect": "reads",
          "facts": [
            "Host",
            "Slug",
            "Name",
            "Heading",
            "Title",
            "Content",
            "Locale",
            "Publication date",
            "Hold date",
            "Edit message",
            "Tags",
            "Weight",
            "Robots",
            "Canonical URL",
            "Template",
            "Custom properties",
            "Social metadata",
            "Parent",
            "Inherited Page",
            "Main image",
            "Variant master",
            "Translations",
            "Redirect paths"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "cms-api::editorial"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/PageResolver.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/PageController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Repository/PageRepository.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/PageApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Entity/Review.php"
    }
  ]
}
---

# Read page — raw page

## Trigger

Read page through editorial API using the raw page way.

## Outcome

The selected content is returned as canonical raw frontmatter and body. Draft, scheduled and held values are included; dynamic public-resolution predicates do not filter this editorial read.
