---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "page"
    },
    {
      "type": "entity",
      "id": "redirection"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Entity/Page.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/EventListener/PageListener.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Repository/PageRepository.php"
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

# Logical content kind can change while record identity persists

Supported body/destination changes can change an existing content record between ordinary Page and redirect-only meaning while retaining record identity. Projection into these two Product nouns does not create two database records.
