---
{
  "availability": [
    {
      "place": "administration::editorial"
    },
    {
      "place": "cms-api::editorial"
    },
    {
      "place": "operator-cli"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/StaticController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/Controller/Api/StaticApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/StaticCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/StaticAppGenerator.php"
    }
  ]
}
---

# Generate static site

Generate a whole static site and retain observable scope-specific status and output. This is generation, not a guarantee of deployment.

## Established boundaries

- The retained completed status can represent a no-longer-running process; consult reported output and errors rather than treating it as proof of successful generation.
