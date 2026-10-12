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

# Page and Redirection API updates require the current revision

The supported Page/Redirection update requires the current revision. Missing revision produces the missing-precondition outcome; a stale revision produces conflict without overwriting current scalar content. The inspected DELETE path does not require the same revision.
