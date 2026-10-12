---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "image",
      "facts": [
        "Rights values",
        "Licensing origin"
      ]
    },
    {
      "type": "entity",
      "id": "file",
      "facts": [
        "Rights values",
        "Licensing origin"
      ]
    }
  ],
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
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/EventListener/MediaLicenseStateListener.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/EventListener/MediaNamingListener.php"
    }
  ]
}
---

# Rights changes preserve the inspected provenance contract

Eligible Vich raster uploads import recognized metadata or apply the supported rights seed. A byte-identical replacement preserves human values; a genuinely new replacement clears/reseeds according to its path. Human changes become overridden and clearing becomes absent. Non-raster files do not acquire automatic raster seeding. Rotation bypasses that upload seed path. Public image structured data requires its inspected minimum rights values and does not prove legal ownership.
