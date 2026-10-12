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
      "text": "The observed IP/host throttle refuses the submission without another saved entry.",
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

# Submit message — rate limit

## Trigger

Submit message through public website using the rate limit way.

## Outcome

The observed IP/host throttle refuses the submission without another saved entry.
