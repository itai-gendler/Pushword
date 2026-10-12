---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "message",
      "effect": "changes",
      "contexts": [
        {
          "place": "website::public::conversation"
        },
        {
          "place": "website::signed-in::conversation"
        }
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "visitor"
      ]
    },
    {
      "actors": [
        "user"
      ]
    },
    {
      "actors": [
        "editor"
      ]
    },
    {
      "actors": [
        "administrator"
      ]
    },
    {
      "actors": [
        "super-administrator"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Controller/ConversationFormController.php"
    }
  ]
}
---

# Public and signed-in form users may change submissions

The configured public and signed-in form contracts accept submissions. Continuation identity is bound workflow proof, not server-side Account ownership.
