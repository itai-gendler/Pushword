---
{
  "type": "web",
  "actors": [
    "visitor",
    "user",
    "editor",
    "administrator",
    "super-administrator"
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/PageController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Controller/ConversationFormController.php"
    }
  ]
}
---

# Website

Public Page reading, discovery and conversation submission, with signed-in reading and editorial preview.
