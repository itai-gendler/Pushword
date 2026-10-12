---
{
  "availability": [
    {
      "place": "administration::editorial"
    },
    {
      "place": "cms-api::editorial"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/PageCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/MediaCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/PageApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/PageRedirectionApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/MediaApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/snippet/src/Controller/Api/SnippetApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Controller/Api/ConversationApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/Controller/Api/ReviewApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/EventSubscriber/FlatWebhookLockSubscriber.php"
    }
  ]
}
---

# Edit content

Change the supported facts of an existing editorial record. Form saves, direct toggles, raw replacement and API merge/patch ways preserve their distinct contracts.

## Established boundaries

- A Message API changes content, author/contact, referrer, host, locale, tags and readable non-null publication values; it does not expose media or arbitrary custom-property editing.
- A Review API changes its supported body/title/rating/reply/contact/host/locale/referrer/translation/publication values. It does not inherit Message tags or media parity.
- The specialized Redirection API changes destination and response code with its current-revision check, rather than offering arbitrary Page-field updates.

## Field acceptance

The Page API uses the frontmatter/body mapping for its supported content, address, publication, hold, metadata and registered relationship values; replacement resets supported omitted values while patch/merge preserves its own selective contract. The Media API accepts alternative and localized text, tags, custom-property merging/removal, filename history and renaming, with raster rotation handled separately. Ordinary media forms and the stronger uploader accept their displayed metadata and rights values. Identity references are selection values, not editable fields. Only the Page pre-update listener establishes ordinary automatic timestamp and current-account attribution; the shared timestamp trait does not establish that behavior for every record kind.
