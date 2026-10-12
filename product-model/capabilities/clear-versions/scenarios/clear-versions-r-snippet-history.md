---
{
  "kind": "primary",
  "routes": {
    "main": "Editorial administration"
  },
  "steps": [
    {
      "kind": "actor",
      "actor": "administrator",
      "text": "Submit the selected history clearing with request proof.",
      "entities": [],
      "contexts": {
        "main": {
          "place": "administration::editorial::versions"
        }
      }
    },
    {
      "kind": "product",
      "actor": "administrator",
      "text": "The selected reusable-content snapshots are removed and the actor is carried to its live editing context.",
      "entities": [
        {
          "entity": "snippet-version",
          "effect": "removes"
        }
      ],
      "contexts": {
        "main": {
          "place": "administration::editorial::versions"
        }
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/VersionController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/version/src/Versionner.php"
    }
  ]
}
---

# Clear versions — snippet history

## Trigger

Clear versions through editorial administration using the snippet history way.

## Outcome

The selected reusable-content snapshots are removed and the actor is carried to its live editor.
