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

# Recent matching submissions can succeed without duplication

Matching content and author contact within ten minutes can return success without another saved entry. The inspected duplicate match is not host-scoped.
