---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "page",
      "facts": [
        "Host",
        "Slug"
      ]
    },
    {
      "type": "entity",
      "id": "redirection",
      "facts": [
        "Host",
        "Slug"
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
    }
  ]
}
---

# Content addresses are unique within a host

A Page or Redirection address is unique within its stored host. Raw host strings do not establish configured-site identity. Supported validation rejects an occupied host/slug combination.
