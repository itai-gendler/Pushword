---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "template",
      "effect": "creates",
      "contexts": [
        {
          "place": "administration::editorial::templates"
        },
        {
          "place": "administration::editorial::template"
        }
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
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/template-editor/src/ElementRepository.php"
    }
  ]
}
---

# Only Administrator, Super Administrator may create Template

Ordinary template administration uses the stronger role; creation and removal also depend on the retained restriction. Super Administrators bypass ordinary selection and creation restrictions.
