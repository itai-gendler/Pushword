---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "delete-page",
      "contexts": [
        {
          "place": "cms-api::editorial"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/PageApiController.php"
    }
  ]
}
---

# Hard deletion moves the old path to an existing destination

Hard deletion removes the source when the destination is an existing internal page that is not itself a redirect; that destination gains the old path and response code. Any other supported destination keeps the source as a published redirect-only record.
