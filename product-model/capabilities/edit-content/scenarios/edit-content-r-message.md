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
      "text": "Edit the selected conversation entry’s body, attribution, host, referrer, tags, weight and custom properties.",
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
      "text": "Accepted body, attribution, host, referrer, tags, weight and custom-property edits are saved on the selected entry.",
      "entities": [
        {
          "entity": "message",
          "effect": "changes",
          "facts": [
            "Content",
            "Author name",
            "Author email",
            "Host",
            "Referring value",
            "Tags",
            "Weight",
            "Custom properties"
          ]
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
      "target": "packages/admin/src/Controller/MediaCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/PageApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/PageRedirectionApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/MediaApiController.php"
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

# Edit content — message

## Trigger

Edit content through editorial administration using the message way.

## Outcome

Accepted body, attribution, host, referrer, tags, weight and custom-property edits are saved on the selected entry.
