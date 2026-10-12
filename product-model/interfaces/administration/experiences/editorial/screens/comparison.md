---
{
  "entities": [
    {
      "entity": "page-version",
      "shows": [
        "Version reference",
        "Captured at",
        "Captured editor",
        "Captured values"
      ]
    },
    {
      "entity": "snippet-version",
      "shows": [
        "Version reference",
        "Captured at",
        "Captured editor",
        "Captured values"
      ]
    },
    {
      "entity": "page",
      "shows": [
        "Heading",
        "Title",
        "Content",
        "Slug",
        "Custom properties"
      ],
      "collects": [
        "Content",
        "Heading",
        "Title",
        "Slug",
        "Custom properties"
      ]
    },
    {
      "entity": "redirection",
      "shows": [
        "Heading",
        "Slug",
        "Destination",
        "Custom properties"
      ],
      "collects": [
        "Heading",
        "Slug",
        "Destination",
        "Custom properties"
      ]
    },
    {
      "entity": "snippet",
      "shows": [
        "Name",
        "Content",
        "Slug",
        "Custom properties"
      ],
      "collects": [
        "Name",
        "Content",
        "Slug",
        "Custom properties"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/VersionController.php#compareVersion"
    }
  ]
}
---

# Comparison

The selected historical comparison against current live or another historical value, including its supported editable scalar fields and unmanaged properties.
