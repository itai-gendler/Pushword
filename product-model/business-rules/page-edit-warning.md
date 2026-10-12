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
      "target": "packages/admin/src/Controller/PageLockController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Service/PageEditLockManager.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/PageCrudController.php"
    }
  ]
}
---

# Editing notices remain advisory

Editing presence and newer-save notices are advisory. They do not themselves prevent saving and do not replace revision or webhook checks. No retained presence Entity or ownership grant is inferred.
