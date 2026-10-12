---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/snippet/src/Entity/Snippet.php"
    }
  ],
  "relations": [
    {
      "entity": "snippet-version",
      "verb": "has-history",
      "cardinality": "one-to-many"
    }
  ]
}
---

# Snippet

Reusable content addressed by a host and slug.

## Information kept

- **Reference** — The subject identity used to select this instance.
- **Host** — The stored host value; it need not identify a currently configured Site.
- **Slug** — The normalized host-scoped content address.
- **Name** — The maintained editorial name, breadcrumb name or reusable-content label.
- **Content** — The maintained body content.
- **Tags** — The retained subject tags used by the supported filtering/rendering contracts.
- **Custom properties** — The retained named extension values, accepted or merged only through the supported entry path.
- **Created at** — The retained created at for this snippet.
- **Updated at** — The retained updated at for this snippet.
