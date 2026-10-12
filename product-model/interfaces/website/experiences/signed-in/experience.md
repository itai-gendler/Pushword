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

# Signed in

Signed-in reading and submission; editorial preview is governed separately.
