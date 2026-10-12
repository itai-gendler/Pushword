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

# Administrator

A person with the shipped stronger administration privilege.
