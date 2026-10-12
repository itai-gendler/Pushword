---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Resources/config/packages/security.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Scheduler/CronScheduleProvider.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/template-editor/src/ElementAdmin.php"
    }
  ],
  "singleton": true
}
---

# Product settings

The Product’s retained deployment configuration, maintained outside the mapped inbound operations.

## Information kept

- **Editorial timezone** — The clock zone interpreting offsetless editorial date input.
- **Password reset enabled** — Whether the forgot-password request path is enabled; setup-link handling is separate.
- **OAuth configuration** — The configured provider access methods matching existing accounts.
- **Installed extensions** — The configured optional bundles; this does not assert a deployed set.
- **Scheduled commands** — Configured commands dispatched by the publication and cron paths.
- **Search settings** — Configured indexing/query behavior for the installed search extension.
- **Scanner settings** — Configured scan coordination, interval and selection settings.
- **Template creation restricted** — Whether ordinary template creation, removal and path movement are disabled; Super Administrators bypass this restriction.
- **Editable template paths** — The configured selection of existing templates; an empty list selects all.
