---
{
  "kind": "edge",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Submit the selected changes through the specified edit path.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::redirection"
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
          "place": "administration::editorial::redirection"
        }
      },
      "actor": "editor"
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The same record identity becomes ordinary content when the supported body change selects that logical kind. Installed version capture retains the resulting distinct scalar snapshot.",
      "entities": [
        {
          "entity": "redirection",
          "effect": "changes",
          "facts": [
            "Destination",
            "Updated at",
            "Last editor"
          ]
        },
        {
          "entity": "page",
          "effect": "changes",
          "facts": [
            "Content",
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
          "place": "administration::editorial::redirection"
        }
      }
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
      "target": "packages/admin/src/FormField/PageMainContentField.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Entity/Page.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/Versionner.php"
    }
  ]
}
---

# Edit content — redirection becomes page

## Trigger

An Editor replaces a redirect-only record’s Location: body with ordinary content through the Redirection editor’s main-content input.

## Outcome

The same record identity becomes ordinary content when the supported body change selects that logical kind. The Page and Redirection entries describe logical views of the same stored record; no additional row is created or removed.
