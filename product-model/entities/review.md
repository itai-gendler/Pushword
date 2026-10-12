---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Entity/Review.php"
    }
  ],
  "relations": [
    {
      "entity": "image",
      "verb": "attaches",
      "cardinality": "many-to-many"
    },
    {
      "entity": "file",
      "verb": "attaches",
      "cardinality": "many-to-many"
    }
  ]
}
---

# Review

An independently addressed review with inherited conversation facts and additional rating, reply and localized content. API field acceptance differs from the Message API.

## Information kept

- **Reference** — The subject identity used to select this instance.
- **Content** — The maintained body content.
- **Author name** — The submitted or editorially supplied author name.
- **Author email** — The submitted contact value; the newsletter-request form can also use its supported phone value.
- **Author IP** — The retained anonymized author address information.
- **Referring value** — The retained submission/referrer value used by applicable conversation selection.
- **Host** — The stored host value; it need not identify a currently configured Site.
- **Locale** — The retained content or site locale, independent of the interface translation set.
- **Publication date** — The retained publication date; its interpretation follows the relevant publication rule.
- **Deleted at** — The retained tombstone date; the row remains while mapped non-deleted queries exclude it.
- **Created at** — The retained created at for this review.
- **Updated at** — The retained updated at for this review.
- **Tags** — The retained subject tags used by the supported filtering/rendering contracts.
- **Weight** — The retained editorial ordering or weighting value.
- **Custom properties** — The retained named extension values, accepted or merged only through the supported entry path.
- **Media** — The retained conversation media relationships; API field acceptance is separate.
- **Title** — The maintained search/document title or review title for this subject.
- **Rating** — The retained optional review rating, validated within one through five when supplied through its API.
- **Reply** — The retained review reply, removable through its supported input contract.
- **Reply author** — The retained reply attribution, with the inspected configured default when absent.
- **Localized title/content** — The retained locale-keyed review title and body values.

## States

### Unpublished

Publication date is absent and the entry is not tombstoned.

### Published

Publication date is present; the public query does not require it to be due.

### Deleted

Deleted at is present; mapped public and API queries exclude the entry.
