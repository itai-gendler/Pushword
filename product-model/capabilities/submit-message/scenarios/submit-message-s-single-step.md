---
{
  "kind": "primary",
  "routes": {
    "main": "Signed-in website"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "user",
      "text": "Submit the configured form stage and its supplied continuation proof.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "website::signed-in::conversation"
        }
      }
    },
    {
      "kind": "product",
      "actor": "user",
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
          "place": "website::signed-in::conversation"
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

Submit message through signed-in website using the single step way.

## Outcome

A valid configured single-stage submission is persisted and returns its supported success outcome.
