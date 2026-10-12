---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "page-redirect",
      "effect": "removes",
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

# Only Site Operator may remove Page redirect

Supported deployment-level Page and former-path operations require no CMS session; the Product also reads publication facts in its own configured due-date check.
