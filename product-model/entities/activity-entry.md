---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/Admin/VersionLogCrudController.php"
    }
  ]
}
---

# Activity entry

A denormalized, observable record of a versionable action, retained independently of the live subject.

## Information kept

- **Subject reference** — The saved subject identity addressed by this record.
- **Type** — The captured subject kind in the activity entry.
- **Action** — The captured versionable creation, update or restoration action.
- **Version reference** — The identity selecting this retained historical snapshot.
- **Editor** — The editor identity recorded in observable activity.
- **Title** — The maintained search/document title or review title for this subject.
- **Slug** — The normalized host-scoped content address.
- **Host** — The stored host value; it need not identify a currently configured Site.
- **Date** — The recorded date of the observable action.
