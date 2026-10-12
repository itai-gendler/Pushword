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
          "place": "administration::editorial::review"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The selected review is tombstoned and excluded from the mapped non-deleted queries.",
      "entities": [
        {
          "entity": "review",
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
          "place": "administration::editorial::review"
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

# Delete content — review

## Trigger

Delete content through editorial administration using the review way.

## Outcome

The selected review is tombstoned and excluded from the mapped non-deleted queries.
