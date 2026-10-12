---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "snippet"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/snippet/src/Entity/Snippet.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/snippet/src/Controller/Api/SnippetApiController.php"
    }
  ]
}
---

# Reusable content follows the inspected fallback order

Runtime resolution considers the component-specific way, host-specific stored content, global stored content and finally empty fallback in the inspected order. This does not imply that every renderer supports every extension shortcode.
