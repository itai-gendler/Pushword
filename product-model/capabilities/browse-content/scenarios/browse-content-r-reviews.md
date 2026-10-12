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
      "text": "The selected review collection returns the supported list facts through its own administration contract.",
      "entities": [
        {
          "entity": "review",
          "effect": "reads",
          "facts": [
            "Content",
            "Title",
            "Rating",
            "Author name",
            "Reply",
            "Locale",
            "Publication date",
            "Created at",
            "Updated at"
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

# Browse content — reviews

## Trigger

Browse content through editorial administration using the reviews way.

## Outcome

The selected review collection returns the supported list facts through its own administration contract.
