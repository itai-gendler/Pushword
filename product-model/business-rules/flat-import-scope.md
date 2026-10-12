---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "import-pages",
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
      "target": "packages/flat/src/Command/FlatFileSyncCommand.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Sync/PageSync.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/flat/src/Service/FlatLockManager.php"
    }
  ]
}
---

# Flat import scope determines reset and missing-file handling

Full import processes supported redirect definitions before Page Markdown, protects backup/snippet directories and protects malformed-file addresses from the missing-file deletion sweep. Forced full import resets applicable content; targeted import does not imply full redirect processing or broad missing-file deletion. Explicit frontmatter slug takes precedence over the filename; the observed timestamp/default/author behavior differs from form construction. The command’s supplied/default webhook check occurs before canonical-host iteration and force does not bypass it.
