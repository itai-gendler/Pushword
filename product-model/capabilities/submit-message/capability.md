---
{
  "availability": [
    {
      "place": "website::public"
    },
    {
      "place": "website::signed-in"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Controller/ConversationFormController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Entity/Message.php"
    }
  ]
}
---

# Submit message

Submit a configured conversation form, including multistep and newsletter-request ways, and receive its submission outcome.

## Established boundaries

- Configuration chooses the supported form; signed-in submission preserves the inspected author-field behavior rather than creating a different submission capability.
