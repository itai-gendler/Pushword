---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/Versionner.php"
    }
  ],
  "domain": "pages"
}
---

# Page version

One retained scalar snapshot of a Page or Redirection. Captured values include scalar content, address, publication, hold and edit-message values; associations are not reconstructed.

## Information kept

- **Version reference** — The identity selecting this retained historical snapshot.
- **Captured at** — The snapshot’s retained capture date.
- **Captured editor** — The editor identity captured for the historical record when available.
- **Captured values** — The recorded scalar values of this snapshot’s subject.
