---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Entity/Message.php"
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

# Message

A submitted or editorially maintained conversation entry. Deletion is a tombstone and does not remove the row.

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
- **Created at** — The retained created at for this message.
- **Updated at** — The retained updated at for this message.
- **Tags** — The retained subject tags used by the supported filtering/rendering contracts.
- **Weight** — The retained editorial ordering or weighting value.
- **Custom properties** — The retained named extension values, accepted or merged only through the supported entry path.
- **Media** — The retained conversation media relationships; API field acceptance is separate.

## States

### Unpublished

Publication date is absent and the entry is not tombstoned.

### Published

Publication date is present; the public query does not require it to be due.

### Deleted

Deleted at is present; mapped public and API queries exclude the entry.
