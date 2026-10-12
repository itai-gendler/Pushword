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
          "place": "administration::editorial::reviews"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The review publication date is made present.",
      "entities": [
        {
          "entity": "review",
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
      "target": "packages/api/src/Service/PageFrontmatterMapper.php"
    }
  ]
}
---

# Publish content — review

## Trigger

Publish content through editorial administration using the review way.

## Outcome

The review publication date is made present.
