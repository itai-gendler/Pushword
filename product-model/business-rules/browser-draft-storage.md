---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "restore-unsaved-page-changes",
      "contexts": [
        {
          "place": "administration::editorial"
        }
      ]
    },
    {
      "type": "capability",
      "id": "discard-unsaved-page-changes",
      "contexts": [
        {
          "place": "administration::editorial"
        }
      ]
    },
    {
      "type": "capability",
      "id": "sign-out",
      "contexts": [
        {
          "place": "administration::account"
        },
        {
          "place": "administration::editorial"
        }
      ]
    }
  ],
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
  ]
}
---

# Recovery restores changed form fields without saving content

Local recovery keys include editor and saved subject identities, including redirect-only editors. Changed recoverable values are saved after the observed debounce, with editor normalization before baseline measurement. Applying recovery fills form fields without a database save; files/request-proof values are excluded. Successful save cleans the subject copy; logout-link cleanup removes all matching origin copies, while session expiry alone leaves them. A changed baseline warns rather than silently overwriting server content.
