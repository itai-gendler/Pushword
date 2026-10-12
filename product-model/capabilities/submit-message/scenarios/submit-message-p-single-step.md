---
{
  "kind": "primary",
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
      "text": "A valid configured single-stage submission is persisted and returns its supported success outcome.",
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

# Submit message — single step

## Trigger

Submit message through public website using the single step way.

## Outcome

A valid configured single-stage submission is persisted and returns its supported success outcome.
