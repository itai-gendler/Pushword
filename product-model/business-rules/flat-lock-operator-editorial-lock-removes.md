---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "editorial-lock",
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
      "target": "packages/flat/src/Command/FlatLockCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Command/FlatUnlockCommand.php"
    }
  ]
}
---

# Only Site Operator may remove Editorial lock

The operator lock contract supports its kind-specific acquisition and any-kind release without CMS session or owner-only release.
