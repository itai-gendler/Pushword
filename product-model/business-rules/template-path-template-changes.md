---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "template",
      "effect": "changes",
      "contexts": [
        {
          "place": "administration::editorial::template"
        }
      ],
      "facts": [
        "Path"
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "administrator"
      ],
      "when": [
        {
          "entity": "product-settings",
          "fact": "Template creation restricted",
          "is": false
        }
      ]
    },
    {
      "actors": [
        "super-administrator"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/template-editor/src/ElementAdmin.php"
    }
  ]
}
---

# Template path changes follow administrator privilege and creation restrictions

Existing-template movement is disabled for ordinary administrators under the creation restriction; the shipped unrestricted override bypasses it.
