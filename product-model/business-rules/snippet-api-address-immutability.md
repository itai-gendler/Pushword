---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "edit-content",
      "contexts": [
        {
          "place": "administration::editorial"
        },
        {
          "place": "cms-api::editorial"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/snippet/src/Controller/Api/SnippetApiController.php"
    }
  ]
}
---

# Snippet API updates preserve host and slug

The inspected Snippet API update ignores host/slug address changes and writes only its supported name/body/tags values. This does not remove administration address editing.
