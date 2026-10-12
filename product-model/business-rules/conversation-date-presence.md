---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "message",
      "facts": [
        "Publication date"
      ]
    },
    {
      "type": "entity",
      "id": "review",
      "facts": [
        "Publication date"
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

# Public conversation selection checks publication presence

The inspected public selection requires a present publication date and no tombstone; it does not require the date to be due. API omitted or null publication input preserves the existing date, so null input does not offer API unpublication. Referrer/tag queries do not establish universal host isolation.
