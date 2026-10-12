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
      "text": "Submit removal of the selected asset link.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::message"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "Invalid detachment proof leaves the relationship unchanged.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::message"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Controller/Admin/ConversationCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Controller/Admin/ReviewCrudController.php"
    }
  ]
}
---

# Remove conversation media — invalid csrf

## Trigger

Remove conversation media through editorial administration using the invalid csrf way.

## Outcome

Invalid detachment proof leaves the relationship unchanged.
