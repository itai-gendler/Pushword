---
{
  "kind": "primary",
  "routes": {
    "main": "Operator CLI"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "site-operator",
      "text": "Request reconciliation of the specified scope.",
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
      "text": "The selected host is reconciled in both directions using the inspected change detector. Installed version capture retains the resulting distinct scalar snapshot.",
      "entities": [
        {
          "entity": "page",
          "effect": "changes",
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
          ]
        },
        {
          "entity": "redirection",
          "effect": "changes",
          "facts": [
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
          "entity": "page-redirect",
          "effect": "changes",
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
          ],
          "as": "page-snapshot"
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
          "as": "redirection-snapshot"
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

# Synchronize pages — explicit host

## Trigger

Synchronize pages through operator CLI using the explicit host way.

## Outcome

The selected host is reconciled in both directions using the inspected change detector.
