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
          "place": "administration::editorial::pages"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The selected page collection returns the supported list facts through its own administration contract.",
      "entities": [
        {
          "entity": "page",
          "effect": "reads",
          "facts": [
            "Slug",
            "Heading",
            "Publication date",
            "Hold date",
            "Tags",
            "Weight",
            "Updated at",
            "Last editor"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::pages"
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

# Browse content — pages

## Trigger

Browse content through editorial administration using the pages way.

## Outcome

The selected page collection returns the supported list facts through its own administration contract.
