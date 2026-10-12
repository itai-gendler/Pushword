---
{
  "entities": [
    {
      "entity": "page",
      "shows": [
        "Host",
        "Slug",
        "Updated at"
      ]
    },
    {
      "entity": "redirection",
      "shows": [
        "Host",
        "Slug",
        "Destination",
        "Updated at"
      ]
    },
    {
      "entity": "page-redirect",
      "shows": [
        "Source path",
        "Response code"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Command/FlatFileSyncCommand.php"
    }
  ]
}
---

# Page transfer

The filesystem/database transfer process showing scope, direction, conflict outcomes and findings.
