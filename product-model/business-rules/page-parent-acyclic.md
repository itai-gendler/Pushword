---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "page",
      "facts": [
        "Parent"
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

# Page parenting rejects self and ancestral cycles

Parent assignment rejects the Page itself and an ancestor cycle. This does not assert the same cycle check for the separate inheritance relationship.
