---
{
  "type": "web",
  "actors": [
    "user",
    "editor",
    "administrator",
    "super-administrator"
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
      "target": "packages/admin/src/Controller/DashboardController.php"
    }
  ]
}
---

# Administration

Account access and the restricted editorial CMS.
