---
{
  "availability": [
    {
      "place": "operator-cli"
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

# Check scheduled publications

Check due publication changes and conditionally dispatch configured commands. The Product also starts the configured scheduled check unattended.
