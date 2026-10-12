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
      "text": "Request selected-content output generation.",
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
      "text": "The selected content generation follows supported entry checks and downstream selection, and can also produce its own feed.",
      "entities": [
        {
          "entity": "page",
          "effect": "reads",
          "facts": [
            "Host",
            "Slug",
            "Content",
            "Publication date",
            "Hold date",
            "Custom properties"
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
      "target": "packages/static-generator/src/Controller/Api/StaticApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/StaticCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/Generator/PageGenerator.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/StaticAppGenerator.php"
    }
  ]
}
---

# Generate static page — selected generation

## Trigger

Generate static page through editorial API using the selected generation way.

## Outcome

The selected content generation follows supported entry checks and downstream selection, and can also produce its own feed.

The synchronous API response does not initialize or update the background scope’s Status or Output, or advance Last full generation. Applicable per-Page rendering state and generated files are delivery data outside that retained process-information contract.
