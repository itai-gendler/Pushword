---
{
  "availability": [
    {
      "place": "administration::login"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/UserController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Service/MagicLinkMailer.php"
    }
  ],
  "domain": "users"
}
---

# Reset password

Request an enabled password-reset link and complete replacement of the same Account’s password.
