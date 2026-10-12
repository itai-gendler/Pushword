---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Resources/assets/admin.unsavedChanges.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/templates/page/edit.html.twig"
    }
  ],
  "domain": "pages"
}
---

# Browser draft

An origin-local unsaved copy keyed by editor and saved Page or Redirection. Its associations describe recovery keys and do not establish server ownership.

## Information kept

- **Editor reference** — The editor identity included in the origin-local recovery key.
- **Subject reference** — The saved subject identity addressed by this record.
- **Changed fields** — Recoverable form values differing from the baseline, excluding files and request-proof inputs.
- **Baseline** — The form values against which unsaved changes were measured.
- **Saved at** — The time recorded with this origin-local copy.
