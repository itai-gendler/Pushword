---
{
  "kind": "edge",
  "routes": {
    "main": "Operator CLI"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "site-operator",
      "text": "Request the specified filesystem-to-database transfer.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "operator-cli::page-transfer"
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
          "place": "operator-cli::page-transfer"
        }
      },
      "actor": "site-operator"
    },
    {
      "kind": "product",
      "actor": "site-operator",
      "text": "An explicit draft publication value creates or retains content without a publication date. Installed version capture retains the resulting distinct scalar snapshot.",
      "entities": [
        {
          "entity": "page",
          "effect": "creates",
          "facts": [
            "Reference",
            "Host",
            "Slug",
            "Name",
            "Heading",
            "Title",
            "Content",
            "Locale",
            "Publication date",
            "Hold date",
            "Created at",
            "Updated at",
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
            "Redirect paths",
            "Creator",
            "Last editor"
          ],
          "to": "Draft"
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
          "with": "page"
        }
      ],
      "contexts": {
        "main": {
          "place": "operator-cli::page-transfer"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Command/FlatFileSyncCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Sync/PageSync.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Service/FlatLockManager.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/Versionner.php"
    }
  ]
}
---

# Import pages — explicit draft

## Trigger

Import pages through operator CLI using the explicit draft way.

## Outcome

An explicit draft publication value creates or retains content without a publication date.
