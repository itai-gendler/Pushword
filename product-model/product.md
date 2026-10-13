---
{
  "id": "pushword",
  "summary": "A modular CMS for maintaining multisite, multilingual Pages, media and reusable content.",
  "category": "content-management-system",
  "license": "MIT",
  "languages": [
    "en",
    "fr"
  ],
  "limitations": [
    "Signing in with an OAuth provider admits only accounts that already exist; it never creates users.",
    "When accounts are kept in a flat users file, that file is their source of truth and passwords are never synced from it.",
    "Administration, the CMS API, search, static generation and versions come from bundles a site installs one by one.",
    "Page content is Markdown with front matter rendered through Twig templates; there is no field builder."
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Entity/Page.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Resources/config/packages/security.php"
    }
  ]
}
---

# Pushword

A modular CMS for multisite, multilingual Pages, media and reusable content. Its supported interactions include public reading and submission, editorial administration, the CMS API and deployment-level commands. Optional bundles provide the corresponding behavior when installed and configured. Content locales and site rendering remain configurable.

## Intent

Pushword lets content editors and site administrators create, manage and maintain one or more multilingual websites from a single application, whether they work in the admin, in Git or through an AI agent.
