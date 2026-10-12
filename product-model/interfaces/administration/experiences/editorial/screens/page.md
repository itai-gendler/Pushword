---
{
  "entities": [
    {
      "entity": "page",
      "shows": [
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
      "collects": [
        "Host",
        "Slug",
        "Name",
        "Heading",
        "Title",
        "Content",
        "Locale",
        "Publication date",
        "Hold date",
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
        "Redirect paths"
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
      "entity": "page-redirect",
      "shows": [
        "Source path",
        "Response code"
      ],
      "collects": [
        "Source path",
        "Response code"
      ]
    },
    {
      "entity": "redirection",
      "collects": [
        "Destination",
        "Response code"
      ]
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
      "target": "packages/admin/src/DependencyInjection/Configuration.php"
    }
  ]
}
---

# Page

An addressed content context. Public reading exposes rendered content and applicable conversation values; the editorial context edits supported content facts, links and preview/recovery inputs.
