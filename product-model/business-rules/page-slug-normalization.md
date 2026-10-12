---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "page",
      "facts": [
        "Slug"
      ]
    },
    {
      "type": "entity",
      "id": "redirection",
      "facts": [
        "Slug"
      ]
    },
    {
      "type": "entity",
      "id": "page-redirect",
      "facts": [
        "Source path"
      ]
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

# Content paths use the supported normalization

Slug handling lowercases and normalizes supported numeric and nested paths while allowing the inspected underscore and dot forms. Leading/trailing path slashes normalize; isolated dot or parent segments fail the slug validator. Former paths use their own normalized ordering and response-code mapping.
