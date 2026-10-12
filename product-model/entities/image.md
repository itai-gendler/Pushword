---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Entity/Media.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/EventListener/MediaLicenseSeedListener.php"
    }
  ],
  "relations": [
    {
      "entity": "page",
      "verb": "is-main-image-of",
      "cardinality": "one-to-many"
    }
  ],
  "domain": "media"
}
---

# Image

An independently addressable raster image with descriptive, storage and image-specific information.

## Information kept

- **Reference** — The subject identity used to select this instance.
- **Filename** — The retained media address name used by storage and lookup.
- **Filename history** — Earlier media names retained for supported historical-name lookup.
- **Stored file** — The retained asset content and its storage association.
- **MIME type** — The detected media type used by supported file/image behavior.
- **Size** — The retained asset size information.
- **Content hash** — The retained current-content digest used by duplicate detection.
- **Original hash** — The retained original-content digest used by applicable media processing.
- **Alternative text** — The maintained descriptive alternative text.
- **Localized text** — The retained locale-specific descriptive media values.
- **Tags** — The retained subject tags used by the supported filtering/rendering contracts.
- **Inherited tags** — Usage-derived tags maintained from the inspected content relationships.
- **Hidden from administration** — Whether the media is hidden by the supported administration selection.
- **Custom properties** — The retained named extension values, accepted or merged only through the supported entry path.
- **Created at** — The retained created at for this image.
- **Updated at** — The retained updated at for this image.
- **Dimensions** — The raster width and height retained for image processing and filtering.
- **Color information** — The retained raster color/preview information.
- **Rights values** — Retained creator, credit, copyright, license and acquisition values; no ownership guarantee.
- **Licensing origin** — Imported, seeded, third-party, overridden or absent rights provenance as recorded by the inspected paths.
