---
{
  "entities": [
    {
      "entity": "message",
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
        "Created at"
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
        "Custom properties"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Controller/Admin/ConversationCrudController.php"
    }
  ]
}
---

# Message

The selected conversation editor collecting its supported content, contact, moderation and relationship values.
