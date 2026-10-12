---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "page",
      "effect": "reads",
      "contexts": [
        {
          "place": "operator-cli"
        }
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "site-operator"
      ]
    },
    {
      "unattended": true
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Command/FlatFileSyncCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Command/DeletePageCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Command/CronCommand.php"
    }
  ]
}
---

# Site operators and configured publication checks read Pages

Supported deployment-level Page and former-path operations require no CMS session; the Product also reads publication facts in its own configured due-date check.
