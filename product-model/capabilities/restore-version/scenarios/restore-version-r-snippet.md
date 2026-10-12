---
{
  "kind": "primary",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "administrator",
      "text": "Submit the selected restoration with request proof.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::versions"
        }
      }
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "Captured reusable-content scalar values are restored and the actor is carried to its live editing context.",
      "entities": [
        {
          "entity": "snippet",
          "effect": "changes",
          "facts": [
            "Host",
            "Slug",
            "Name",
            "Content",
            "Tags",
            "Custom properties",
            "Created at",
            "Updated at"
          ]
        },
        {
          "entity": "snippet-version",
          "effect": "reads",
          "facts": [
            "Captured values"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::versions"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/VersionController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/Versionner.php"
    }
  ]
}
---

# Restore version — snippet

## Trigger

Restore version through editorial administration using the snippet way.

## Outcome

Captured reusable-content scalar values are restored and the actor is carried to its live editor.
