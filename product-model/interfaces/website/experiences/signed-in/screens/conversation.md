---
{
  "entities": [
    {
      "entity": "message",
      "collects": [
        "Content",
        "Author name",
        "Author email",
        "Referring value"
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

# Conversation

A configured submission process retaining its single-stage or multistage progress and submission outcome.
