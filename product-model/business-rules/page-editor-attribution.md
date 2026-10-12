---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "page",
      "facts": [
        "Creator",
        "Last editor",
        "Created at",
        "Updated at"
      ]
    },
    {
      "type": "entity",
      "id": "redirection",
      "facts": [
        "Creator",
        "Last editor",
        "Created at",
        "Updated at"
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

# Applicable content writes stamp their observed attribution

The inspected save paths stamp creation/editor/timestamp information where applicable. Unattended or filesystem paths use their observed author fallback rather than inventing an initiating CMS account.
