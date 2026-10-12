---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "browser-draft",
      "effect": "reads",
      "contexts": [
        {
          "place": "administration::editorial"
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
      "target": "packages/admin/src/Resources/assets/admin.unsavedChanges.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/templates/page/edit.html.twig"
    }
  ]
}
---

# Only Editor, Administrator, Super Administrator may read Browser draft

Editorial forms recover origin-local copies. Editor/subject keys identify copies but establish no additional server ownership restriction. Logout-link cleanup can remove all matching copies.
