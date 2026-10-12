---
{
  "entities": [
    {
      "entity": "account",
      "collects": [
        "Email",
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
