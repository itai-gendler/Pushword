---
{
  "kind": "edge",
  "routes": {
    "main": "Public website"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "visitor",
      "text": "Submit the configured form stage and its supplied continuation proof.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "website::public::conversation"
        }
      }
    },
    {
      "kind": "product",
      "actor": "visitor",
      "text": "The submission is accepted without establishing delivery when the relevant notification configuration is absent.",
      "entities": [
        {
          "entity": "message",
          "effect": "creates",
          "facts": [
            "Reference",
            "Content",
            "Author name",
            "Author email",
            "Author IP",
            "Referring value",
            "Host",
            "Locale",
            "Publication date",
            "Deleted at",
            "Created at",
            "Updated at",
            "Tags",
            "Weight",
            "Custom properties",
            "Media"
          ],
          "to": "Unpublished"
        }
      ],
      "contexts": {
        "main": {
          "place": "website::public::conversation"
        }
      }
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

# Submit message — notification unconfigured

## Trigger

Submit message through public website using the notification unconfigured way.

## Outcome

The submission is accepted without establishing delivery when the relevant notification configuration is absent.
