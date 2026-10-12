---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "submit-message",
      "contexts": [
        {
          "place": "website::public"
        },
        {
          "place": "website::signed-in"
        }
      ]
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
      "target": "packages/conversation/src/Controller/Api/ConversationApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Controller/Api/ReviewApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Controller/Api/PublishedAtPayloadTrait.php"
    }
  ]
}
---

# Continuation proof binds the saved submission and stage

A multistep continuation uses temporary proof bound to the saved subject, step, form type, referrer and host with the inspected one-hour lifetime. Each accepted stage can persist partial values. This is not ownership by a CMS Account.
