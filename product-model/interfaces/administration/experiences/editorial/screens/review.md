---
{
  "entities": [
    {
      "entity": "review",
      "shows": [
        "Content",
        "Author name",
        "Author email",
        "Author IP",
        "Referring value",
        "Host",
        "Publication date",
        "Tags",
        "Weight",
        "Custom properties",
        "Created at",
        "Title",
        "Rating",
        "Reply",
        "Reply author",
        "Locale",
        "Media"
      ],
      "collects": [
        "Content",
        "Author name",
        "Author email",
        "Author IP",
        "Referring value",
        "Host",
        "Publication date",
        "Tags",
        "Weight",
        "Custom properties",
        "Title",
        "Rating",
        "Reply",
        "Reply author",
        "Locale",
        "Media"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Controller/Admin/ReviewCrudController.php"
    }
  ]
}
---

# Review

The selected rated-entry editor collecting its supported review, reply, locale and asset relationship values.
