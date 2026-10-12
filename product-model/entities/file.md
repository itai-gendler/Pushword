---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Entity/Media.php"
    }
  ],
  "domain": "media"
}
---

# File

An independently addressable non-raster file with descriptive and storage information.

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
- **Created at** — The retained created at for this file.
- **Updated at** — The retained updated at for this file.
- **Rights values** — Retained creator, credit, copyright, license and acquisition values; no ownership guarantee.
- **Licensing origin** — Imported, seeded, third-party, overridden or absent rights provenance as recorded by the inspected paths.
