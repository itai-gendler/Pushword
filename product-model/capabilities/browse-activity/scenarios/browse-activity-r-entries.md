---
{
  "kind": "primary",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Request the retained action collection.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::activity"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The retained denormalized action facts are returned, including subjects whose live record no longer exists.",
      "entities": [
        {
          "entity": "activity-entry",
          "effect": "reads",
          "facts": [
            "Subject reference",
            "Type",
            "Action",
            "Version reference",
            "Editor",
            "Title",
            "Slug",
            "Host",
            "Date"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::activity"
        }
      }
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

# Browse activity — entries

## Trigger

Browse activity through editorial administration using the entries way.

## Outcome

The retained denormalized action facts are returned, including subjects whose live record no longer exists.
