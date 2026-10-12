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
      "text": "Submit the new source path and content.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::template"
        }
      }
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "New-path intake can replace the source already at that path; this does not take the existing-source rename collision check.",
      "entities": [
        {
          "entity": "template",
          "effect": "changes",
          "facts": [
            "Source"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::template"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/template-editor/src/ElementAdmin.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/template-editor/src/Element.php"
    }
  ]
}
---

# Create template — existing intake path

## Trigger

An Administrator enters Template creation while Template creation restricted is false and supplies a Path already occupied by a Template, plus replacement Source. The original-path editable list does not select creation destinations.

## Outcome

The existing Template’s Source is overwritten at its unchanged Path. No second retained Template is created, and the existing-source rename collision check does not run. Applicable Twig cache is cleared and rendering invalidated; the response carries the Administrator to the editor for that Path.
