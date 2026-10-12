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
      "text": "Clear the publication value.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::messages"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The administration moderation operation clears the conversation publication date.",
      "entities": [
        {
          "entity": "message",
          "effect": "changes",
          "facts": [
            "Publication date"
          ],
          "to": "Unpublished",
          "from": "Published"
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::messages"
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

# Unpublish conversation — message

## Trigger

Unpublish conversation through editorial administration using the message way.

## Outcome

The administration moderation operation clears the conversation publication date.
