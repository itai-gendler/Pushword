---
{
  "type": "api",
  "actors": [
    "visitor",
    "editor",
    "administrator",
    "super-administrator"
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/DocsApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Security/ApiTokenAuthenticator.php"
    }
  ]
}
---

# CMS API

Supported documentation, identity, content, lock and processing contracts.
