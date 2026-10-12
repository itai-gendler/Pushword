---
{
  "kind": "primary",
  "result": "achieved",
  "routes": {
    "main": "Product hand-off"
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
      },
      "capability": "create-template"
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "New-path intake stores the accepted source and carries the actor to its editing context.",
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
      },
      "capability": "create-template"
    },
    {
      "kind": "product",
      "actor": "administrator",
      "capability": "create-template",
      "text": "The Product carries the person to the newly saved source’s editing context.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::template"
        }
      }
    },
    {
      "kind": "actor",
      "actor": "administrator",
      "text": "Submit the selected source, comparison or uploader changes.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::template"
        }
      },
      "capability": "edit-administrative-content"
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "Accepted source changes are stored and applicable rendering caches are invalidated.",
      "entities": [
        {
          "entity": "template",
          "effect": "changes",
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
      },
      "capability": "edit-administrative-content"
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
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/MediaMultiUploadController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/VersionController.php"
    }
  ]
}
---

# Edit new template — template

## Trigger

Continue editing the newly created source.

## Outcome

The accepted source exists and its editor accepts further source changes.
