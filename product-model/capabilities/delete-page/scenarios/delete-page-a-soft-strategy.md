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
      "text": "Request the selected deletion strategy with its destination or confirmation.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "cms-api::editorial"
        }
      }
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
          "place": "cms-api::editorial"
        }
      },
      "actor": "editor"
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The retained redirect-only record clears publication instead of universally erasing its fallback redirect. Installed version capture retains the resulting distinct scalar snapshot.",
      "entities": [
        {
          "entity": "redirection",
          "effect": "changes",
          "facts": [
            "Destination",
            "Response code",
            "Publication date",
            "Updated at",
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
      "target": "packages/api/src/Controller/PageApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Command/DeletePageCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/PageCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/Versionner.php"
    }
  ]
}
---

# Delete page — soft strategy

## Trigger

Delete page through editorial API using the soft strategy way.

## Outcome

The retained redirect-only record clears publication instead of universally erasing its fallback redirect.
