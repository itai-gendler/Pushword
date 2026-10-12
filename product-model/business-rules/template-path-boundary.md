---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "create-template",
      "contexts": [
        {
          "place": "administration::editorial"
        }
      ]
    },
    {
      "type": "capability",
      "id": "edit-administrative-content",
      "contexts": [
        {
          "place": "administration::editorial"
        }
      ]
    },
    {
      "type": "capability",
      "id": "delete-administrative-content",
      "contexts": [
        {
          "place": "administration::editorial"
        }
      ]
    },
    {
      "type": "capability",
      "id": "browse-administrative-content",
      "contexts": [
        {
          "place": "administration::editorial"
        }
      ]
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
      "target": "packages/template-editor/src/ElementRepository.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/template-editor/src/Element.php"
    }
  ]
}
---

# Template paths follow selection and movement constraints

Existing source selection uses the configured editable list; empty means all and the shipped Super Administrator override bypasses the ordinary list and creation restriction. Paths containing parent traversal are refused. Existing-source movement onto an occupied target is refused, but new-path intake can overwrite source at an existing path. Movement/storage failure is not asserted atomic.
