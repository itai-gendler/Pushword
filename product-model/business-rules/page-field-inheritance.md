---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "page",
      "facts": [
        "Main image",
        "Template",
        "Custom properties",
        "Inherited Page"
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

# Page inheritance covers only the inspected fallback fields

The inspected fallback relationship can inherit main image, template and custom-property values. It is not inheritance of every Page fact or body, and no additional inheritance-cycle guarantee is inferred.
