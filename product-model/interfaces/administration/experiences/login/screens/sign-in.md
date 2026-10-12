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

# Sign in

The existing-profile access process, including password, emailed access and configured provider ways.
