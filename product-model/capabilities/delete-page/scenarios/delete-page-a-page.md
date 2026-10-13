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
      "text": "Delete the selected published source with an existing internal non-redirect destination that does not yet own its path.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "cms-api::editorial"
        }
      }
    },
    {
      "kind": "condition",
      "text": "Delete strategy is Hard (the default).",
      "entities": [
        {
          "entity": "product-settings",
          "effect": "reads",
          "facts": [
            "Delete strategy"
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
      "text": "For hard deletion with an existing internal non-redirect destination, the source is removed and its former path and response code are added to the destination. Installed version capture retains the resulting distinct scalar snapshot.",
      "entities": [
        {
          "entity": "page",
          "effect": "removes",
          "as": "source",
          "from": "Published"
        },
        {
          "entity": "page",
          "effect": "changes",
          "as": "destination",
          "facts": [
            "Redirect paths",
            "Updated at",
            "Last editor"
          ]
        },
        {
          "entity": "page-redirect",
          "effect": "creates",
          "facts": [
            "Source path",
            "Response code"
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

# Delete page — page

## Trigger

Delete page through editorial API using the page way.

## Outcome

For hard deletion with an existing internal non-redirect destination, the source is removed and its former path and response code are added to the destination.
