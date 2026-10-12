---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/Controller/Api/StaticApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/static-generator/src/GenerationStateManager.php"
    }
  ]
}
---

# Static generation

The latest retained generation status and output for a scope. Completed status alone is not proof of successful rendered output, and retained job history is not promised.

## Information kept

- **Scope** — The retained operation scope or normalized lock key.
- **Status** — The latest reported processing state; it is not a delivery guarantee.
- **Output** — The latest retained processing output for the addressed scope.
- **Errors** — The retained generation error information available through its status contract.
- **Last full generation** — The retained full-generation time; all-host reporting uses the oldest host and can be absent if any host lacks a completed full generation.
