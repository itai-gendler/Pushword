---
{
  "entities": [
    {
      "entity": "page",
      "shows": [
        "Name",
        "Heading",
        "Title",
        "Content",
        "Slug",
        "Locale",
        "Main image",
        "Translations"
      ]
    },
    {
      "entity": "message",
      "shows": [
        "Content",
        "Author name",
        "Publication date"
      ]
    },
    {
      "entity": "review",
      "shows": [
        "Title",
        "Content",
        "Rating",
        "Reply",
        "Reply author",
        "Localized title/content"
      ]
    },
    {
      "entity": "site",
      "shows": [
        "Host",
        "Locale",
        "Base URL"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/PageResolver.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/PageController.php"
    }
  ]
}
---

# Page

An addressed content context. Public reading exposes rendered content and applicable conversation values; the editorial context edits supported content facts, links and preview/recovery inputs.
