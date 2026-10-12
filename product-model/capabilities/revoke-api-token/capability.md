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
      "target": "packages/admin/src/Controller/UserCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Entity/User.php"
    }
  ],
  "domain": "users"
}
---

# Revoke api token

Clear the Account form’s token candidate and persist the revocation with the saved Account.
