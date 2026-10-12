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
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/template-editor/src/DependencyInjection/Configuration.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/template-editor/src/config/services.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/template-editor/src/ElementAdmin.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/template-editor/src/ElementRepository.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/template-editor/src/Element.php"
    }
  ],
  "permits": [
    {
      "configuredBy": "product-settings"
    },
    {
      "actors": [
        "super-administrator"
      ]
    }
  ]
}
---

# Template changes follow operation settings, with a Super Administrator bypass

The customer's Template creation restricted and Editable template paths settings evaluate the actual requested operation.

For creation intake, including intake that overwrites Source at an existing Path, configuration permits the operation only when Template creation restricted is false. Editable template paths is not consulted to admit the chosen creation-intake destination.

For entry through an existing-template editor, the initially selected file must belong to Editable template paths, unless that list is empty. Template creation restricted does not prohibit ordinary Source editing. Existing-template renaming retains its separate Path permission and validation. Selection checks the original file; it does not add an allowlist check on the rename destination.

Super Administrators bypass both customer restrictions. Passing this configuration Rule does not replace the independent administrative role permission.
