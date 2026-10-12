---
{
  "entities": [
    {
      "entity": "account",
      "shows": [
        "Password change required"
      ],
      "collects": [
        "Password"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/UserController.php"
    }
  ]
}
---

# Password

The credential replacement process collecting the supplied replacement and confirmation or reset-request contact.
