---
{
  "availability": [
    {
      "place": "administration::account"
    },
    {
      "place": "administration::editorial"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Resources/config/packages/security.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Resources/assets/admin.unsavedChanges.js"
    }
  ],
  "domain": "users"
}
---

# Sign out

End the current CMS session. The administration logout-link path also clears matching origin-local unsaved copies.
