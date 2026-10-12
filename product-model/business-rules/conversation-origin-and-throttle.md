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

# Submissions follow configured origin and throttle checks

Configured allowed-origin handling rejects a disallowed supplied origin while the absent-origin path can proceed. The observed IP/host submission checks throttle excess requests; workflow and form validation still apply.
