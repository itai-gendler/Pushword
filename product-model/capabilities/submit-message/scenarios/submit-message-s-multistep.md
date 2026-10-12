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
      "text": "The first valid stage persists an unpublished submission and returns continuation proof bound to its saved identity and next stage.",
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
    },
    {
      "kind": "actor",
      "actor": "user",
      "text": "Submit author email and name with the bound continuation proof.",
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
      "text": "The accepted continuation updates the same saved submission and consumes the workflow proof at completion.",
      "entities": [
        {
          "entity": "message",
          "effect": "changes",
          "facts": [
            "Content",
            "Author email",
            "Author name"
          ]
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
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Form/AbstractConversationForm.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Form/MultiStepMessageForm.php"
    }
  ]
}
---

# Submit message — multistep

## Trigger

Submit message through signed-in website using the multistep way.

## Outcome

The first valid stage creates one unpublished submission. The bound continuation updates that same submission and consumes its proof on completion.
