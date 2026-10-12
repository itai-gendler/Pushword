---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "edit-content",
      "contexts": [
        {
          "place": "administration::editorial"
        },
        {
          "place": "cms-api::editorial"
        }
      ]
    },
    {
      "type": "capability",
      "id": "delete-content",
      "contexts": [
        {
          "place": "administration::editorial"
        },
        {
          "place": "cms-api::editorial"
        }
      ]
    },
    {
      "type": "capability",
      "id": "upload-media",
      "contexts": [
        {
          "place": "administration::editorial"
        },
        {
          "place": "cms-api::editorial"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/EventListener/MediaUsageListener.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Entity/Media.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/conversation/src/EventListener/MediaListCleanupListener.php"
    }
  ]
}
---

# Media relationships preserve inspected cleanup and usage tags

Inspected content/media relationship maintenance clears removed main-image references, detaches conversation galleries and refreshes derived/inherited usage tags. Complete extractor vocabulary and picker hand-offs are not established by these effects.
