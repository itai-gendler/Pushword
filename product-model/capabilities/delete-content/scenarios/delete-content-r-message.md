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
      "text": "Request removal of the selected record.",
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
      "text": "The selected message is tombstoned and excluded from the mapped non-deleted queries.",
      "entities": [
        {
          "entity": "message",
          "effect": "changes",
          "facts": [
            "Deleted at",
            "Updated at"
          ],
          "to": "Deleted",
          "from": "Published"
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
      "target": "packages/admin/src/Controller/MediaCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/MediaApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Controller/Api/ConversationApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/EventListener/MediaListCleanupListener.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/snippet/src/Controller/Api/SnippetApiController.php"
    }
  ]
}
---

# Delete content — message

## Trigger

Delete content through editorial administration using the message way.

## Outcome

The selected message is tombstoned and excluded from the mapped non-deleted queries.
