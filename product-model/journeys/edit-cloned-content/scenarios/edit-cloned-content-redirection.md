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
      "text": "Request a draft copy of the selected content.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::redirection"
        }
      },
      "capability": "clone-page"
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
      "capability": "clone-page"
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "A redirect-only copy is created with publication cleared and a copy address, and the editing context is carried to it; fallback redirect eligibility remains separate. Installed version capture retains the resulting distinct scalar snapshot.",
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
      "capability": "clone-page"
    },
    {
      "kind": "product",
      "actor": "editor",
      "capability": "clone-page",
      "text": "The Product carries the editing context to the new copy’s live editing context.",
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
      "text": "Submit the selected changes through the specified edit path.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::redirection"
        }
      },
      "capability": "edit-content"
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The accepted redirection fields are saved through its own administration contract; unaccepted fields do not gain interface parity. Installed version capture retains the resulting distinct scalar snapshot.",
      "entities": [
        {
          "entity": "redirection",
          "effect": "changes",
          "facts": [
            "Host",
            "Slug",
            "Destination",
            "Response code",
            "Publication date",
            "Hold date",
            "Custom properties",
            "Updated at",
            "Last editor"
          ]
        },
        {
          "entity": "browser-draft",
          "effect": "removes"
        },
        {
          "entity": "page-version",
          "effect": "creates",
          "facts": [
            "Version reference",
            "Captured at",
            "Captured editor",
            "Captured values"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::redirection"
        }
      },
      "capability": "edit-content"
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
      "target": "packages/core/src/Service/VariantManager.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/MediaCrudController.php"
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
      "target": "packages/api/src/Controller/MediaApiController.php"
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
      "target": "packages/version/src/Versionner.php"
    }
  ]
}
---

# Edit cloned content — redirection

## Trigger

Edit the newly cloned content.

## Outcome

The copy is open in its editor and accepted supported changes are saved.
