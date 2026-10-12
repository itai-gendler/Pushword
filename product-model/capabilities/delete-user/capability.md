---
{
  "availability": [
    {
      "place": "administration::editorial"
    },
    {
      "place": "operator-cli"
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
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Command/UserDeleteCommand.php"
    }
  ],
  "domain": "users"
}
---

# Delete user

Remove an existing CMS Account through administration or the operator command.
