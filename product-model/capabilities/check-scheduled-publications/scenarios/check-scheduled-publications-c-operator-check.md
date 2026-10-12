---
{
  "kind": "primary",
  "routes": {
    "main": "Operator CLI"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "site-operator",
      "text": "Request the configured due-publication check.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "operator-cli"
        }
      }
    },
    {
      "kind": "product",
      "actor": "site-operator",
      "text": "The due-date watermark is checked and configured publication commands are dispatched for eligible changes.",
      "entities": [
        {
          "entity": "page",
          "effect": "reads",
          "facts": [
            "Host",
            "Publication date"
          ]
        },
        {
          "entity": "product-settings",
          "effect": "reads",
          "facts": [
            "Scheduled commands"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "operator-cli"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Command/CronCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Scheduler/CronScheduleProvider.php"
    }
  ]
}
---

# Check scheduled publications — operator check

## Trigger

Check scheduled publications through operator CLI using the operator check way.

## Outcome

The due-date watermark is checked and configured publication commands are dispatched for eligible changes.
