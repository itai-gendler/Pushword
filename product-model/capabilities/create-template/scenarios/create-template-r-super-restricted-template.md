---
{
  "kind": "primary",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "super-administrator",
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
      "actor": "super-administrator",
      "text": "The shipped unrestricted override creates the accepted source despite ordinary creation restrictions.",
      "entities": [
        {
          "entity": "template",
          "effect": "creates",
          "facts": [
            "Path",
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

# Create template — super restricted template

## Trigger

Create template through editorial administration using the super restricted template way.

## Outcome

The shipped unrestricted override creates the accepted source despite ordinary creation restrictions.
