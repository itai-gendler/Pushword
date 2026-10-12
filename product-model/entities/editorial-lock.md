---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Service/FlatLockManager.php"
    }
  ]
}
---

# Editorial lock

A retained filesystem editing lock addressed by its normalized scope key, including literal default. Its kind, expiry and release contracts differ by entry path.

## Information kept

- **Scope** — The retained operation scope or normalized lock key.
- **Kind** — Lock classification selected by the stored reason and creation path.
- **Reason** — The retained lock reason that can determine manual/webhook/automatic classification.
- **Acquired at** — The retained lock-acquisition time used with its lifetime.
- **TTL** — The retained lifetime used by expiry lookup.
- **Locked by** — The retained holder description; release is not universally owner-only.
