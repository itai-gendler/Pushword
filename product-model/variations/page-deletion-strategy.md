---
kind: configuration
of: business-rule
settings:
  - { entity: product-settings, fact: Delete strategy }
takesEffect: When the Page API handles a deletion. The strategy is deployment configuration, so a change applies to deletions after the configuration is reloaded.
stability: Pages already deleted keep the outcome of the strategy in force at the time; a change does not convert existing records.
alternatives:
  - id: page-api-hard-deletion
    selectedWhen: Delete strategy is Hard. Missing strategy uses Hard.
  - id: page-api-soft-deletion
    selectedWhen: Delete strategy is Soft.
---

# Page deletion strategy

Deployments choose what the Page API does with a deleted page's record; both policies are supported.
