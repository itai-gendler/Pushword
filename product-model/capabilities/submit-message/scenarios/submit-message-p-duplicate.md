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
      "text": "Matching recent content and contact can return success without creating a second entry; the inspected matching window is ten minutes and is not host-scoped.",
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

# Submit message — duplicate

## Trigger

Submit message through public website using the duplicate way.

## Outcome

Matching recent content and contact can return success without creating a second entry; the inspected matching window is ten minutes and is not host-scoped.
