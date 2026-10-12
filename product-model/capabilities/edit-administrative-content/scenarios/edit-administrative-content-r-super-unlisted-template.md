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
      "text": "Read the selected Template’s Path and Source, then submit revised Source at the existing Path of a Template omitted from the ordinary editable list.",
      "entities": [
        {
          "entity": "template",
          "effect": "reads",
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
    },
    {
      "kind": "product",
      "actor": "super-administrator",
      "text": "The Product stores Source at the unchanged Path and invalidates applicable rendering caches.",
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
      "target": "packages/admin/src/Controller/MediaMultiUploadController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/VersionController.php"
    },
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

# Edit administrative content — unlisted template by Super Administrator

## Trigger

A Super Administrator opens an existing Template whose Path is absent from a non-empty Editable template paths list and submits revised Source without changing Path.

## Outcome

The submitted Source is stored at that Path, applicable Twig cache is cleared and rendering invalidated.
