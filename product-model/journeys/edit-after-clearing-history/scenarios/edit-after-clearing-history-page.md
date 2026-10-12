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
      "actor": "administrator",
      "text": "Submit the selected history clearing with request proof.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::versions"
        }
      },
      "capability": "clear-versions"
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "The selected content subject’s snapshots are removed and the actor is carried to its live editing context.",
      "entities": [
        {
          "entity": "page-version",
          "effect": "removes"
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::versions"
        }
      },
      "capability": "clear-versions"
    },
    {
      "kind": "product",
      "actor": "administrator",
      "capability": "clear-versions",
      "text": "The Product carries the person to the live editing context after clearing history.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::versions"
        }
      }
    },
    {
      "kind": "actor",
      "actor": "administrator",
      "text": "Submit the selected changes through the specified edit path.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::page"
        }
      },
      "capability": "edit-content"
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
          "place": "administration::editorial::page"
        }
      },
      "actor": "administrator",
      "capability": "edit-content"
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "Accepted heading, title and body values are saved; the update timestamp and current attribution are recorded. Other values stay as supplied by this entry path’s contract. Installed version capture retains the resulting distinct scalar snapshot.",
      "entities": [
        {
          "entity": "page",
          "effect": "changes",
          "facts": [
            "Heading",
            "Title",
            "Content",
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
          "place": "administration::editorial::page"
        }
      },
      "capability": "edit-content"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/VersionController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/Versionner.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/PageCrudController.php"
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
    }
  ]
}
---

# Edit after clearing history — page

## Trigger

Continue editing after clearing the selected history.

## Outcome

The selected history is cleared and the live editor accepts supported changes.
