---
{
  "availability": [
    {
      "place": "administration::editorial"
    },
    {
      "place": "cms-api::editorial"
    },
    {
      "place": "operator-cli"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/PageApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Command/DeletePageCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/PageCrudController.php"
    }
  ]
}
---

# Delete page

Delete selected Pages or Redirections through administration, destination-aware API strategies or confirmed tag-scoped operator deletion.

## Established boundaries

- Administration and confirmed operator removal apply to selected drafts and scheduled content as well as the published primary example; no API destination or revision contract is inferred for those ways.
- The specialized Redirection API removal is direct; destination-aware deletion belongs to the Page API strategy.
