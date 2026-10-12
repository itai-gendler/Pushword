---
{
  "kind": "edge",
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
          "place": "administration::editorial::medium"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "Removing media detaches affected conversation gallery relationships.",
      "entities": [
        {
          "entity": "image",
          "effect": "removes"
        },
        {
          "entity": "message",
          "effect": "changes",
          "facts": [
            "Media"
          ]
        },
        {
          "entity": "review",
          "effect": "changes",
          "facts": [
            "Media"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::medium"
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

# Delete content — conversation media detached

## Trigger

Delete content through editorial administration using the conversation media detached way.

## Outcome

Removing media detaches affected conversation gallery relationships.
