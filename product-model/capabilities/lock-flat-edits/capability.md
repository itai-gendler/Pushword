---
{
  "availability": [
    {
      "place": "cms-api::editorial"
    },
    {
      "place": "operator-cli"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Controller/FlatLockApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Command/FlatLockCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Service/FlatLockManager.php"
    }
  ]
}
---

# Lock flat edits

Acquire or replace an editing lock for its normalized scope through the API or operator contract.
