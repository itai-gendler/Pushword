---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Entity/Page.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/PageRedirectionApiController.php"
    }
  ],
  "relations": [
    {
      "entity": "page-redirect",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "page-version",
      "verb": "has-history",
      "cardinality": "one-to-many"
    },
    {
      "entity": "browser-draft",
      "verb": "has-unsaved-changes",
      "cardinality": "one-to-many"
    }
  ],
  "domain": "pages"
}
---

# Redirection

An addressable redirect-only Page, identified by the same record while its logical content kind can change.

## Information kept

- **Reference** — The subject identity used to select this instance.
- **Host** — The stored host value; it need not identify a currently configured Site.
- **Slug** — The normalized host-scoped content address.
- **Destination** — The retained redirect destination encoded by the redirect-only content.
- **Response code** — The retained redirect response code, with path-specific accepted/default values.
- **Heading** — The maintained main heading used in editorial/public content.
- **Locale** — The retained content or site locale, independent of the interface translation set.
- **Publication date** — The retained publication date; its interpretation follows the relevant publication rule.
- **Hold date** — Any non-null value activates the applicable generation hold.
- **Created at** — The retained created at for this redirection.
- **Updated at** — The retained updated at for this redirection.
- **Tags** — The retained subject tags used by the supported filtering/rendering contracts.
- **Weight** — The retained editorial ordering or weighting value.
- **Custom properties** — The retained named extension values, accepted or merged only through the supported entry path.
- **Redirect paths** — The retained former source paths and their response codes.
- **Creator** — The recorded account responsible for creation where the inspected path supplies one.
- **Last editor** — The recorded account responsible for the latest applicable write.
