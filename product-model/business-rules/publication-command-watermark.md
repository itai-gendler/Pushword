---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "check-scheduled-publications",
      "contexts": [
        {
          "place": "operator-cli"
        }
      ]
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

# Publication checks advance their watermark before dispatch

With configured publication commands, first execution initializes the baseline without replaying all past publications. Later checks select newly due publication dates after the last watermark and through now, advance the watermark before command dispatch and dispatch once or per canonical host when a host substitution is configured. The configured publication schedule checks at the inspected 300-second interval; neither retry nor deployment is guaranteed.
