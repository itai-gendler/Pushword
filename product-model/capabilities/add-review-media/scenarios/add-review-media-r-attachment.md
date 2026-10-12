---
{
  "kind": "primary",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Select the existing asset to attach.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::review"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The existing media is attached to the selected review through the inspected editing context relationship.",
      "entities": [
        {
          "entity": "review",
          "effect": "changes",
          "facts": [
            "Media"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::review"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Controller/Admin/ReviewCrudController.php"
    }
  ]
}
---

# Add review media — attachment

## Trigger

Add review media through editorial administration using the attachment way.

## Outcome

The existing media is attached to the selected review through the inspected editor relationship.
