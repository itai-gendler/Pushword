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
      "text": "Set the publication value.",
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
      "text": "The conversation publication date is made present.",
      "entities": [
        {
          "entity": "message",
          "effect": "changes",
          "facts": [
            "Publication date"
          ],
          "to": "Published",
          "from": "Unpublished"
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
      "target": "packages/api/src/Service/PageFrontmatterMapper.php"
    }
  ]
}
---

# Publish content — message

## Trigger

Publish content through editorial administration using the message way.

## Outcome

The conversation publication date is made present.
