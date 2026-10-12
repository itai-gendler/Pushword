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
      "text": "Edit supported values, including the reply and gallery.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::review"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "Accepted body, title, rating, attribution, host, referrer, tags, weight, properties, reply, locale and gallery edits are saved.",
      "entities": [
        {
          "entity": "review",
          "effect": "changes",
          "facts": [
            "Content",
            "Title",
            "Rating",
            "Author name",
            "Author email",
            "Host",
            "Referring value",
            "Tags",
            "Weight",
            "Custom properties",
            "Reply",
            "Reply author",
            "Locale",
            "Media"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::review"
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

# Edit content — review

## Trigger

Edit content through editorial administration using the review way.

## Outcome

Accepted body, title, rating, attribution, host, referrer, tags, weight, properties, reply, locale and gallery edits are saved.
