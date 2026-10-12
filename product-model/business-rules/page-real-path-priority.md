---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "read-page",
      "contexts": [
        {
          "place": "website::public"
        },
        {
          "place": "website::signed-in"
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
      "target": "packages/core/src/Entity/Page.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/EventListener/PageListener.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Repository/PageRepository.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/PageController.php"
    }
  ]
}
---

# Real stored paths precede former-path fallback

A real stored path is considered before former-path fallback, including a real path occupied by a draft. Alias ownership collisions have no established deterministic priority. Redirect fallback is assembled without publication filtering.
