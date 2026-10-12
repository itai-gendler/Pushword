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
      "text": "Captured scalar values are restored and the actor is carried to the live editing context without recreating uncaptured associations or an ordinary new restore snapshot.",
      "entities": [
        {
          "entity": "page",
          "effect": "changes",
          "facts": [
            "Host",
            "Slug",
            "Name",
            "Heading",
            "Title",
            "Content",
            "Locale",
            "Publication date",
            "Hold date",
            "Created at",
            "Updated at",
            "Edit message",
            "Tags",
            "Weight",
            "Robots",
            "Canonical URL",
            "Template",
            "Custom properties",
            "Social metadata",
            "Redirect paths",
            "Last editor"
          ]
        },
        {
          "entity": "page-version",
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

# Restore version — page

## Trigger

Restore version through editorial administration using the page way.

## Outcome

Captured scalar values are restored and the actor is carried to the live editor without recreating uncaptured associations or an ordinary new restore snapshot.
