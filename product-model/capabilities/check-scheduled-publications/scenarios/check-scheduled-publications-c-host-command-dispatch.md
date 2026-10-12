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
      "text": "A configured host substitution dispatches per canonical host; other configured commands run once.",
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
        },
        {
          "entity": "site",
          "effect": "reads",
          "facts": [
            "Host",
            "Aliases"
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

# Check scheduled publications — host command dispatch

## Trigger

Check scheduled publications through operator CLI using the host command dispatch way.

## Outcome

A configured host substitution dispatches per canonical host; other configured commands run once.
