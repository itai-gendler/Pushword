---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "page",
      "facts": [
        "Publication date"
      ]
    },
    {
      "type": "entity",
      "id": "redirection",
      "facts": [
        "Publication date"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Entity/Page.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/EventListener/PageListener.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Repository/PageRepository.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Command/FlatFileSyncCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Sync/PageSync.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Service/FlatLockManager.php"
    }
  ]
}
---

# Page publication eligibility follows its publication date

Null publication means Draft; a future date means Scheduled; a non-null due date means Published for Page eligibility. Ordinary construction starts at now, cloning clears publication, and newly imported content with omitted publication uses its file modification time. Crossing the scheduled instant changes eligibility without writing a separate state.
