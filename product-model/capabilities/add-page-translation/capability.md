---
{
  "availability": [
    {
      "place": "administration::editorial"
    },
    {
      "place": "cms-api::editorial"
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
  ],
  "domain": "pages"
}
---

# Add page translation

Link existing Pages as translations, including supported registered cross-host references.
