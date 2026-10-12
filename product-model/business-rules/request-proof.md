---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "sign-in",
      "contexts": [
        {
          "place": "administration::login"
        }
      ]
    },
    {
      "type": "capability",
      "id": "reset-password",
      "contexts": [
        {
          "place": "administration::login"
        }
      ]
    },
    {
      "type": "capability",
      "id": "change-password",
      "contexts": [
        {
          "place": "administration::account"
        },
        {
          "place": "administration::login"
        }
      ]
    },
    {
      "type": "capability",
      "id": "edit-content",
      "contexts": [
        {
          "place": "administration::editorial"
        },
        {
          "place": "cms-api::editorial"
        }
      ]
    },
    {
      "type": "capability",
      "id": "publish-content",
      "contexts": [
        {
          "place": "administration::editorial"
        },
        {
          "place": "cms-api::editorial"
        }
      ]
    },
    {
      "type": "capability",
      "id": "rotate-image",
      "contexts": [
        {
          "place": "administration::editorial"
        },
        {
          "place": "cms-api::editorial"
        }
      ]
    },
    {
      "type": "capability",
      "id": "upload-multiple-media",
      "contexts": [
        {
          "place": "administration::editorial"
        }
      ]
    },
    {
      "type": "capability",
      "id": "restore-version",
      "contexts": [
        {
          "place": "administration::editorial"
        }
      ]
    },
    {
      "type": "capability",
      "id": "clear-versions",
      "contexts": [
        {
          "place": "administration::editorial"
        }
      ]
    },
    {
      "type": "capability",
      "id": "remove-conversation-media",
      "contexts": [
        {
          "place": "administration::editorial"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Controller/UserController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Entity/User.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Service/MagicLinkMailer.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Controller/PageApiController.php"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/api/src/Service/PageFrontmatterMapper.php"
    },
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

# Requests enforce their applicable identity and input proof

Identity credentials, CSRF, revisions and workflow/input proof are checked by the applicable request paths and produce their distinguished refusals. They are transient proof, not synthetic kept authorization facts and not blanket parity across interfaces.
