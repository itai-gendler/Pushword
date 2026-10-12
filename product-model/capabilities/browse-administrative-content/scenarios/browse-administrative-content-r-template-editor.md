---
{
  "kind": "validation",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Request the selected historical or editable-source collection.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::templates"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The source collection request receives its stronger-context refusal outcome.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::templates"
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
      "target": "packages/template-editor/src/ElementRepository.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/template-editor/src/ElementAdmin.php"
    }
  ]
}
---

# Browse administrative content — template editor

## Trigger

Browse administrative content through editorial administration using the template editor way.

## Outcome

The source collection request receives its stronger-context refusal outcome.
