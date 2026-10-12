---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "page-redirect",
      "effect": "reads",
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
  "permits": [
    {
      "actors": [
        "editor"
      ]
    },
    {
      "actors": [
        "administrator"
      ]
    },
    {
      "actors": [
        "super-administrator"
      ]
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
      "target": "packages/api/src/Service/PageFrontmatterMapper.php"
    }
  ]
}
---

# Only Editor, Administrator, Super Administrator may read Page redirect

The supported former-path list operations follow editorial privilege.
