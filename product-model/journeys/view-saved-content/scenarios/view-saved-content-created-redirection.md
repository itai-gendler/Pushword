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
      "text": "Submit the selected new-content values.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::redirection"
        }
      },
      "capability": "create-content"
    },
    {
      "kind": "condition",
      "text": "Version capture is installed and enabled. This accepted write produces distinct scalar values; retained earlier snapshots are inside the full-retention interval.",
      "entities": [
        {
          "entity": "product-settings",
          "effect": "reads",
          "facts": [
            "Installed extensions"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::redirection"
        }
      },
      "actor": "editor",
      "capability": "create-content"
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The accepted redirection values create an addressed record through its own administration form contract. Installed version capture retains the resulting distinct scalar snapshot.",
      "entities": [
        {
          "entity": "redirection",
          "effect": "creates",
          "facts": [
            "Reference",
            "Host",
            "Slug",
            "Destination",
            "Response code",
            "Heading",
            "Locale",
            "Publication date",
            "Hold date",
            "Created at",
            "Updated at",
            "Tags",
            "Weight",
            "Custom properties",
            "Redirect paths",
            "Creator",
            "Last editor"
          ]
        },
        {
          "entity": "page-version",
          "effect": "creates",
          "facts": [
            "Version reference",
            "Captured at",
            "Captured editor",
            "Captured values"
          ],
          "with": "redirection"
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::redirection"
        }
      },
      "capability": "create-content"
    },
    {
      "kind": "product",
      "actor": "editor",
      "capability": "create-content",
      "text": "The Product’s selected save-and-return action carries the person to the saved address.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::redirection"
        }
      }
    },
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Open the selected content address.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "website::signed-in::page"
        }
      },
      "capability": "read-page"
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The saved redirect-only address produces its applicable redirect response.",
      "entities": [
        {
          "entity": "redirection",
          "effect": "reads",
          "facts": [
            "Slug",
            "Destination",
            "Response code"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "website::signed-in::page"
        }
      },
      "capability": "read-page"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/PageCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/PageRedirectionCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/PageApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Service/PageFrontmatterMapper.php"
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
    },
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
      "target": "packages/conversation/src/Entity/Review.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/Versionner.php"
    }
  ]
}
---

# View saved content — created redirection

## Trigger

Open the result of the save-and-return operation.

## Outcome

The accepted saved content produces its public or applicable preview response.
