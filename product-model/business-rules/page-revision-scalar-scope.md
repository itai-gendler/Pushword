---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "read-page",
      "contexts": [
        {
          "place": "website::public"
        },
        {
          "place": "website::signed-in"
        },
        {
          "place": "cms-api::editorial"
        }
      ]
    },
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

# Page revisions cover the supported scalar representation

Page and Redirection revision values derive from the supported scalar representation. They do not guarantee that every association or rendered-output change alters the revision. Other content APIs do not acquire this revision requirement by analogy.
