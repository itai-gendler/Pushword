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
          "place": "administration::editorial::reviews"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The administration moderation operation clears the review publication date.",
      "entities": [
        {
          "entity": "review",
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
          "place": "administration::editorial::reviews"
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

# Unpublish conversation — review

## Trigger

Unpublish conversation through editorial administration using the review way.

## Outcome

The administration moderation operation clears the review publication date.
