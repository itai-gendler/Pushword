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
      "target": "packages/core/src/EventListener/PageListener.php"
    }
  ],
  "relations": [
    {
      "entity": "page",
      "verb": "parents",
      "cardinality": "one-to-many"
    },
    {
      "entity": "page",
      "verb": "provides-inheritance-to",
      "cardinality": "one-to-many"
    },
    {
      "entity": "page",
      "verb": "is-master-of",
      "cardinality": "one-to-many"
    },
    {
      "entity": "page",
      "verb": "translates",
      "cardinality": "many-to-many"
    },
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

# Page

An addressable content Page. Publication eligibility is derived from its date; holding changes affects generation and does not freeze its current database content.

## Information kept

- **Reference** — The subject identity used to select this instance.
- **Host** — The stored host value; it need not identify a currently configured Site.
- **Slug** — The normalized host-scoped content address.
- **Name** — The maintained editorial name, breadcrumb name or reusable-content label.
- **Heading** — The maintained main heading used in editorial/public content.
- **Title** — The maintained search/document title or review title for this subject.
- **Content** — The maintained body content.
- **Locale** — The retained content or site locale, independent of the interface translation set.
- **Publication date** — The retained publication date; its interpretation follows the relevant publication rule.
- **Hold date** — Any non-null value activates the applicable generation hold.
- **Created at** — The retained created at for this page.
- **Updated at** — The retained updated at for this page.
- **Edit message** — The retained edit message for this page.
- **Tags** — The retained subject tags used by the supported filtering/rendering contracts.
- **Weight** — The retained editorial ordering or weighting value.
- **Robots** — The retained indexing directives used by supported output and index selection.
- **Canonical URL** — The configured canonical address override for the Page.
- **Template** — The retained template choice, with applicable inherited fallback.
- **Custom properties** — The retained named extension values, accepted or merged only through the supported entry path.
- **Social metadata** — The retained social-output property values; no universal editor disclosure is promised.
- **Parent** — The retained Page parent used by applicable hierarchy/discovery behavior.
- **Inherited Page** — The retained fallback source for the inspected image/template/custom-property inheritance.
- **Main image** — The selected media reference used as the Page’s main image.
- **Variant master** — The retained master association; a master has no variant-of association.
- **Translations** — The linked translation group, including supported cross-host registered references.
- **Redirect paths** — The retained former source paths and their response codes.
- **Creator** — The recorded account responsible for creation where the inspected path supplies one.
- **Last editor** — The recorded account responsible for the latest applicable write.

## States

### Published

A non-null publication date is due; ordinary construction starts here.

### Draft

The publication date is absent.

### Scheduled

The publication date is in the future. Eligibility changes with time without a publication-state write.
