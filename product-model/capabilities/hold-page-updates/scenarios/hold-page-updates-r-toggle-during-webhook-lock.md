---
{
  "kind": "edge",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Activate the generation hold.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::pages"
        }
      }
    },
    {
      "kind": "condition",
      "text": "Version capture is installed and enabled. This accepted write produces distinct scalar values; retained earlier snapshots are inside the full-retention interval.",
      "entities": [
        {
          "entity": "product-settings",
          "effect": "reads",
          "facts": [
            "Installed extensions"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::pages"
        }
      },
      "actor": "editor"
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The direct hold toggle saves its value without taking the ordinary form-event webhook guard. Installed version capture retains the resulting distinct scalar snapshot.",
      "entities": [
        {
          "entity": "page",
          "effect": "changes",
          "facts": [
            "Hold date",
            "Updated at",
            "Last editor"
          ]
        },
        {
          "entity": "page-version",
          "effect": "creates",
          "facts": [
            "Version reference",
            "Captured at",
            "Captured editor",
            "Captured values"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::pages"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/PageCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/PageApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Service/PageFrontmatterMapper.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/Versionner.php"
    }
  ]
}
---

# Hold page updates — toggle during webhook lock

## Trigger

Hold page updates through editorial administration using the toggle during webhook lock way.

## Outcome

The direct hold toggle saves its value without taking the ordinary form-event webhook guard.
