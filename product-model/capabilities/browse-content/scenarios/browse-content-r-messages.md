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
          "place": "administration::editorial::messages"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The selected message collection returns the supported list facts through its own administration contract.",
      "entities": [
        {
          "entity": "message",
          "effect": "reads",
          "facts": [
            "Content",
            "Author name",
            "Author email",
            "Referring value",
            "Publication date",
            "Weight",
            "Created at",
            "Updated at"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::messages"
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

# Browse content — messages

## Trigger

Browse content through editorial administration using the messages way.

## Outcome

The selected message collection returns the supported list facts through its own administration contract.
