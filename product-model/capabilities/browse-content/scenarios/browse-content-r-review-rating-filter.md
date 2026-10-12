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
      "text": "Request the selected collection and its supported filters.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::reviews"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The administration review collection selects the retained rating property; API reviews without that optional property need not appear in this collection.",
      "entities": [
        {
          "entity": "review",
          "effect": "reads",
          "facts": [
            "Title",
            "Content",
            "Rating",
            "Author name",
            "Reply",
            "Locale",
            "Publication date"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::reviews"
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
    }
  ]
}
---

# Browse content — review rating filter

## Trigger

Browse content through editorial administration using the review rating filter way.

## Outcome

The administration review collection selects the retained rating property; API reviews without that optional property need not appear in this collection.
