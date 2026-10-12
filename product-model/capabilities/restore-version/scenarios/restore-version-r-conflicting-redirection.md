---
{
  "kind": "edge",
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
      "text": "A conflicting redirect record is removed through the special restoration path; ordinary rename handling is suppressed.",
      "entities": [
        {
          "entity": "page",
          "effect": "changes",
          "facts": [
            "Slug",
            "Host",
            "Content",
            "Heading",
            "Title",
            "Publication date",
            "Hold date",
            "Tags",
            "Weight",
            "Robots",
            "Canonical URL",
            "Template",
            "Custom properties",
            "Social metadata",
            "Edit message",
            "Updated at",
            "Last editor"
          ]
        },
        {
          "entity": "redirection",
          "effect": "removes"
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

# Restore version — conflicting redirection

## Trigger

Restore version through editorial administration using the conflicting redirection way.

## Outcome

A conflicting redirect record is removed through the special restoration path; ordinary rename handling is suppressed.
