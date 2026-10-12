---
{
  "availability": [
    {
      "place": "administration::editorial"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/PageCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Service/VariantManager.php"
    }
  ],
  "domain": "pages"
}
---

# Clone page

Create a draft copy of a Page or Redirection and carry the editor to the copy’s editor.

## Established boundaries

- Invalid clone request proof leaves the selected subject uncloned. The fixed copy suffix is not automatically retried after an occupied-address collision.
