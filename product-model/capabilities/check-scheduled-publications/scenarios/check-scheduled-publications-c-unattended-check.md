---
{
  "kind": "primary",
  "routes": {
    "main": "Operator CLI"
  },
  "steps": [
    {
      "kind": "condition",
      "unattended": true,
      "text": "The configured publication schedule starts its due-date check.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "operator-cli"
        }
      }
    },
    {
      "kind": "product",
      "text": "The configured Product schedule performs the same due-publication check without an initiating person.",
      "entities": [
        {
          "entity": "page",
          "effect": "reads",
          "facts": [
            "Host",
            "Publication date"
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

# Check scheduled publications — unattended check

## Trigger

Check scheduled publications through operator CLI using the unattended check way.

## Outcome

The configured Product schedule performs the same due-publication check without an initiating person.
