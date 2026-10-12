---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/PageResolver.php"
    }
  ]
}
---

# Site

One configured site. Host strings on stored content and normalized lock scopes are not assumed to resolve to a configured Site.

## Information kept

- **Host** — The stored host value; it need not identify a currently configured Site.
- **Aliases** — The additional host addresses configured for this Site.
- **Locale** — The retained content or site locale, independent of the interface translation set.
- **Base URL** — The configured public base address used to construct site-aware output.
- **Live URL** — The configured live-site address used by the site contract.
- **Page property declarations** — The configured Page property declarations used by applicable validation/rendering paths.
- **Rendering settings** — Configured templates and rendering options for this Site.
- **Conversation settings** — Configured forms, origins and notification settings for this Site.
