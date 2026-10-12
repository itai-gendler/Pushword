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
          "place": "administration::editorial::review"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The selected media relationship is detached from the review.",
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

# Remove conversation media — review

## Trigger

Remove conversation media through editorial administration using the review way.

## Outcome

The selected media relationship is detached from the review.
