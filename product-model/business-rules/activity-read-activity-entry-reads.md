---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "activity-entry",
      "effect": "reads",
      "contexts": [
        {
          "place": "administration::editorial::activity"
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
      "target": "packages/version/src/Admin/VersionLogCrudController.php"
    }
  ]
}
---

# Only Editor, Administrator, Super Administrator may read Activity entry

The observable activity collection is readable in ordinary editorial administration.
