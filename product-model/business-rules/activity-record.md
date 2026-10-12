---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "page",
      "effect": "creates"
    },
    {
      "type": "entity",
      "id": "page",
      "effect": "changes"
    },
    {
      "type": "entity",
      "id": "redirection",
      "effect": "creates"
    },
    {
      "type": "entity",
      "id": "redirection",
      "effect": "changes"
    },
    {
      "type": "entity",
      "id": "snippet",
      "effect": "creates"
    },
    {
      "type": "entity",
      "id": "snippet",
      "effect": "changes"
    },
    {
      "type": "entity",
      "id": "activity-entry"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/Versionner.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/VersionController.php"
    }
  ]
}
---

# Versionable actions are recorded in activity

Configured version capture records creation, scalar update and restoration activity with the denormalized subject identity, editor, date and relevant version. The observable record can outlive its subject. Logging is automatic processing rather than a separate actor operation.
