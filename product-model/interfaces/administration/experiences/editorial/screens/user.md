---
{
  "entities": [
    {
      "entity": "account",
      "shows": [
        "Email",
        "Username",
        "Interface locale",
        "Roles",
        "Created at",
        "API token"
      ],
      "collects": [
        "Email",
        "Username",
        "Interface locale",
        "Roles",
        "Password",
        "API token"
      ]
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
      "target": "packages/admin/src/DependencyInjection/Configuration.php"
    }
  ]
}
---

# User

The selected profile editor collecting supported profile, locale, role and credential values; retained password material is not disclosed.
