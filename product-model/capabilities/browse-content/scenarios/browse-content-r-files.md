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
          "place": "administration::editorial::media"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The selected file collection returns the supported list facts through its own administration contract.",
      "entities": [
        {
          "entity": "file",
          "effect": "reads",
          "facts": [
            "Alternative text",
            "MIME type",
            "Licensing origin",
            "Updated at",
            "Filename",
            "Tags"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::media"
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

# Browse content — files

## Trigger

Browse content through editorial administration using the files way.

## Outcome

The selected file collection returns the supported list facts through its own administration contract.
