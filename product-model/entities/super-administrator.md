---
{
  "kind": "person",
  "acts": "external",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Resources/config/packages/security.php"
    }
  ],
  "relations": [
    {
      "entity": "account",
      "verb": "uses",
      "cardinality": "one-to-one"
    }
  ]
}
---

# Super Administrator

A person with the shipped account-management privilege.
