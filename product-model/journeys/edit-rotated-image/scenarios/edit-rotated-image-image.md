---
{
  "kind": "primary",
  "result": "achieved",
  "routes": {
    "main": "Product hand-off"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Request the supported rotation.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::medium"
        }
      },
      "capability": "rotate-image"
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "A supported rotation changes raster content and refreshes its applicable derived information/cache.",
      "entities": [
        {
          "entity": "image",
          "effect": "changes",
          "facts": [
            "Stored file",
            "Content hash",
            "Dimensions",
            "Color information",
            "Size"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::medium"
        }
      },
      "capability": "rotate-image"
    },
    {
      "kind": "product",
      "actor": "editor",
      "capability": "rotate-image",
      "text": "The Product carries the person to the rotated asset’s editing context.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::medium"
        }
      }
    },
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Submit the selected changes through the specified edit path.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::medium"
        }
      },
      "capability": "edit-content"
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The supplied descriptive, localized, tag and custom-property values are saved on the selected image; changing its rights values also updates licensing origin.",
      "entities": [
        {
          "entity": "image",
          "effect": "changes",
          "facts": [
            "Alternative text",
            "Localized text",
            "Tags",
            "Custom properties",
            "Rights values",
            "Licensing origin"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::medium"
        }
      },
      "capability": "edit-content"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/MediaCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/MediaApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/PageCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/PageApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/PageRedirectionApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/snippet/src/Controller/Api/SnippetApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Controller/Api/ConversationApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Controller/Api/ReviewApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/EventSubscriber/FlatWebhookLockSubscriber.php"
    }
  ]
}
---

# Edit rotated image — image

## Trigger

Continue editing the rotated asset.

## Outcome

The accepted rotation completes and the returned editor accepts descriptive changes.
