---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "page",
      "effect": "reads",
      "facts": [
        "Content"
      ],
      "contexts": [
        {
          "place": "website::public::page"
        },
        {
          "place": "website::signed-in::page"
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
      "target": "packages/core/src/Controller/PageResolver.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/PageController.php"
    }
  ],
  "permits": [
    {
      "actors": [
        "visitor"
      ],
      "when": [
        {
          "state": "Published"
        }
      ]
    },
    {
      "actors": [
        "user"
      ],
      "when": [
        {
          "state": "Published"
        }
      ]
    },
    {
      "actors": [
        "editor"
      ]
    },
    {
      "actors": [
        "administrator"
      ]
    },
    {
      "actors": [
        "super-administrator"
      ]
    }
  ]
}
---

# Published Page bodies are public; editorial roles also read previews

Visitors and ordinary account holders receive ordinary Published Page content. Actors with effective editorial authority also receive previews, including Draft, Scheduled and future-created Pages. Ordinary content resolution additionally obeys the creation-time visibility constraint; editorial preview bypasses it. The body selector governs Content disclosure, rather than preliminary eligibility inspection.
