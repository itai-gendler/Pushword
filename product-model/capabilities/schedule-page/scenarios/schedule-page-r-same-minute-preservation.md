---
{
  "kind": "edge",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "editor",
      "text": "Resubmit the displayed minute-level publication value without choosing a different minute.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::page"
        }
      }
    },
    {
      "kind": "product",
      "actor": "editor",
      "text": "The Product compares the retained Publication date with the submitted value and preserves the full stored instant, including seconds.",
      "entities": [
        {
          "entity": "page",
          "effect": "reads",
          "facts": [
            "Publication date"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::page"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/FormField/PagePublishedAtField.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Service/EditorialTimezone.php"
    }
  ]
}
---

# Schedule Page — same minute preservation

## Trigger

An Editor resubmits a Scheduled Page’s publication widget at the same displayed minute as its stored Publication date, which includes seconds. No other form value changes.

## Outcome

The stored instant is preserved, including seconds. This request changes neither Publication date nor the derived Scheduled state; it does not truncate the instant or establish another publication update.
