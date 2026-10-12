---
{
  "entities": [
    {
      "entity": "redirection",
      "shows": [
        "Heading",
        "Host",
        "Slug",
        "Destination",
        "Response code",
        "Custom properties"
      ],
      "collects": [
        "Heading",
        "Host",
        "Slug",
        "Destination",
        "Response code",
        "Custom properties"
      ]
    },
    {
      "entity": "browser-draft",
      "shows": [
        "Changed fields",
        "Baseline",
        "Saved at"
      ]
    },
    {
      "entity": "page",
      "shows": [
        "Content"
      ],
      "collects": [
        "Content"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/PageRedirectionCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/DependencyInjection/Configuration.php"
    }
  ]
}
---

# Redirection

The selected redirect-only subject’s editable address, destination and custom values with applicable recovery.
