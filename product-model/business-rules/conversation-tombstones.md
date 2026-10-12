---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "message",
      "facts": [
        "Deleted at"
      ]
    },
    {
      "type": "entity",
      "id": "review",
      "facts": [
        "Deleted at"
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

# Conversation deletion retains a tombstoned record

Deletion retains the record and sets its deletion date. Mapped public and API non-deleted queries exclude tombstones, and repeated API deletion preserves the inspected already-deleted outcome.
