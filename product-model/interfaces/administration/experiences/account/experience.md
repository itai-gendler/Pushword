---
{
  "actors": [
    "user",
    "editor",
    "administrator",
    "super-administrator"
  ],
  "access": "authenticated",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Resources/config/packages/security.php"
    }
  ]
}
---

# Account

Own-account password completion and session ending.
