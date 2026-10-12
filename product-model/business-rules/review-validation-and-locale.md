---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "create-content",
      "contexts": [
        {
          "place": "administration::editorial"
        },
        {
          "place": "cms-api::editorial"
        }
      ]
    },
    {
      "type": "capability",
      "id": "edit-content",
      "contexts": [
        {
          "place": "administration::editorial"
        },
        {
          "place": "cms-api::editorial"
        }
      ]
    },
    {
      "type": "capability",
      "id": "read-page",
      "contexts": [
        {
          "place": "website::public"
        },
        {
          "place": "website::signed-in"
        },
        {
          "place": "cms-api::editorial"
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

# Review rating and locale behavior follow the entry contract

Administration requires a supported rating choice; the Review API rating is optional but checked within one through five when supplied. Accepted locale maps merge, null removes a supplied locale and omitted locales remain. Rendering falls back from regional locale to base locale then original content; a missing reply author can use the configured administration default.
