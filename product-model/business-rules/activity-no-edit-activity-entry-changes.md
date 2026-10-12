---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "activity-entry",
      "effect": "changes",
      "contexts": [
        {
          "place": "administration::editorial::activity"
        }
      ]
    }
  ],
  "permits": [],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/Admin/VersionLogCrudController.php"
    }
  ]
}
---

# Nobody may change Activity entry

The read-only activity controller disables this mutation for every actor.
