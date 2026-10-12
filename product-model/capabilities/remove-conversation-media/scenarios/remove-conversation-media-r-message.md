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
      "text": "The selected media relationship is detached from the conversation entry.",
      "entities": [
        {
          "entity": "message",
          "effect": "changes",
          "facts": [
            "Media"
          ]
        }
      ],
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

# Remove conversation media — message

## Trigger

Remove conversation media through editorial administration using the message way.

## Outcome

The selected media relationship is detached from the conversation entry.
