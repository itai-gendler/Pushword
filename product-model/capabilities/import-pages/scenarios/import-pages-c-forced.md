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
      "text": "Force a full import for a host containing existing published ordinary content and redirect-only records, using accepted input with ordinary content, redirects and former paths.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "operator-cli::page-transfer"
        }
      }
    },
    {
      "kind": "product",
      "actor": "site-operator",
      "text": "With an active webhook lock absent from the command scope, forced full import removes the selected host’s existing content before rebuilding it from accepted Markdown and redirect definitions.",
      "entities": [
        {
          "entity": "page",
          "effect": "removes",
          "as": "old-page",
          "from": "Published"
        },
        {
          "entity": "redirection",
          "effect": "removes"
        },
        {
          "entity": "page-redirect",
          "effect": "removes",
          "with": "old-page"
        }
      ],
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
      "text": "Accepted input recreates the host’s ordinary and redirect-only records with imported address, content, dates, metadata and references. Imported former paths are retained on their new owner. Installed version capture retains the resulting distinct scalar snapshot.",
      "entities": [
        {
          "entity": "page",
          "effect": "creates",
          "as": "imported-page",
          "to": "Published",
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
          ]
        },
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
          "entity": "page-redirect",
          "effect": "creates",
          "with": "imported-page",
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
          "as": "imported-page-snapshot",
          "with": "imported-page"
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
          "as": "redirection-snapshot",
          "with": "redirection"
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

# Import pages — forced

## Trigger

Import pages through operator CLI using the forced way.

## Outcome

Forced full import removes existing host content and rebuilds it from accepted input; the command-level webhook preflight remains effective.
