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
      "text": "Read the selected Template’s Path and Source, then submit updated Source and a different, unoccupied Path for the selected existing Template.",
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
      "actor": "administrator",
      "text": "The Product removes the original stored source, stores the submitted Source at the new Path, clears the applicable Twig cache and invalidates rendering.",
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

# Edit administrative content — template

## Trigger

An Administrator selects an existing Template admitted by Editable template paths, with Template creation restricted false, and submits Source and a different Path without parent traversal or an existing destination file.

## Outcome

The original file is removed and the submitted Source is stored at the new Path. Applicable Twig cache is cleared and rendering is invalidated. The response carries the Administrator to that Template’s editor. Destination membership in Editable template paths is not rechecked during the rename.

## Edge cases

- Editing Source with the original Path stores Source without changing retained Path; the moving-disabled case covers Source editing with the creation restriction active.
- Filesystem or cache-clearing failure does not establish an atomic rename or successful redirect.
