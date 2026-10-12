---
{
  "kind": "validation",
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
          "place": "administration::editorial::pages"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "Invalid proof on the direct publication operation leaves the publication value unchanged.",
      "entities": [],
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
      "target": "packages/api/src/Service/PageFrontmatterMapper.php"
    }
  ]
}
---

# Publish content — page csrf

## Trigger

Publish content through editorial administration using the page csrf way.

## Outcome

Invalid proof on the direct publication operation leaves the publication value unchanged.
