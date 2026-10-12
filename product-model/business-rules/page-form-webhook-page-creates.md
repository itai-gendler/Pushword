---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "page",
      "effect": "creates",
      "contexts": [
        {
          "place": "administration::editorial::page"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/EventSubscriber/FlatWebhookLockSubscriber.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Service/FlatLockManager.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/PageCrudController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/admin/src/Controller/PageRedirectionCrudController.php"
    }
  ]
}
---

# Page form creation stops during an active host webhook workflow

When Page creation is submitted through the EasyAdmin before-persist event, the Product checks the lock scope derived from the record’s raw Host. An active webhook lock prevents that form save. The refusal reports the retained workflow attribution and reason; no Page write occurs through the blocked event.

This concurrent-workflow constraint does not apply to direct operations that do not dispatch the subscribed event, including direct variant promotion, publication and hold toggling. Media returns no host and exits this subscriber without a default-scope check. Existing editorial role permissions remain operative.
