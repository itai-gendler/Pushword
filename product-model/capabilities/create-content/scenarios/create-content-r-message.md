---
{
  "kind": "primary",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Submit the selected new-content values.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::message"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The accepted message values create an addressed record through its own administration form contract.",
      "entities": [
        {
          "entity": "message",
          "effect": "creates",
          "facts": [
            "Reference",
            "Content",
            "Author name",
            "Author email",
            "Author IP",
            "Referring value",
            "Host",
            "Locale",
            "Publication date",
            "Deleted at",
            "Created at",
            "Updated at",
            "Tags",
            "Weight",
            "Custom properties",
            "Media"
          ],
          "to": "Unpublished"
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::message"
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
      "target": "packages/api/src/Controller/PageApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Service/PageFrontmatterMapper.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/snippet/src/Controller/Api/SnippetApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Controller/Api/ConversationApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Controller/Api/ReviewApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/EventSubscriber/FlatWebhookLockSubscriber.php"
    }
  ]
}
---

# Create content — message

## Trigger

Create content through editorial administration using the message way.

## Outcome

The accepted message values create an addressed record through its own administration form contract.
