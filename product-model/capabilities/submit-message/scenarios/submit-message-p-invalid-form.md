---
{
  "kind": "validation",
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
      "text": "Invalid required values leave the stage incomplete and return validation feedback.",
      "entities": [],
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

# Submit message — invalid form

## Trigger

Submit message through public website using the invalid form way.

## Outcome

Invalid required values leave the stage incomplete and return validation feedback.
