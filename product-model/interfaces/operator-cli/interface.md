---
{
  "type": "cli",
  "actors": [
    "site-operator"
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
      "target": "packages/core/src/Command/UserCreateCommand.php"
    }
  ]
}
---

# Operator CLI

Deployment-level operations without CMS sign-in; operating-system access is external to this contract.
