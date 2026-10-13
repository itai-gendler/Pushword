---
{
  "scope": "Initial CMS code across public website, administration, supported CMS API and operator interfaces, with the inspected extension paths.",
  "method": "Static source inspection at commit 2a67018307d097696d8e8008db3c526d62cb2311 and supporting documentation.",
  "covered": [
    {
      "description": "Core entity and addressing code",
      "paths": [
        "packages/core/src/Entity/",
        "packages/core/src/Repository/PageRepository.php",
        "packages/core/src/EventListener/PageListener.php",
        "packages/core/src/Service/VariantManager.php"
      ]
    },
    {
      "description": "Public content and discovery controllers",
      "paths": [
        "packages/core/src/Controller/"
      ]
    },
    {
      "description": "Inspected editorial CRUD and recovery code",
      "paths": [
        "packages/admin/src/Controller/",
        "packages/admin/src/Resources/assets/admin.unsavedChanges.js",
        "packages/admin/src/Service/PageEditLockManager.php",
        "packages/admin/src/templates/page/edit.html.twig"
      ]
    },
    {
      "description": "Account identity and access code",
      "paths": [
        "packages/core/src/Security/",
        "packages/core/src/Controller/UserController.php",
        "packages/core/src/Entity/User.php",
        "packages/core/src/Service/MagicLinkMailer.php",
        "packages/core/src/Resources/config/packages/security.php"
      ]
    },
    {
      "description": "Supported content API handlers and mapping",
      "paths": [
        "packages/api/src/Controller/",
        "packages/api/src/Service/",
        "packages/api/src/Security/",
        "packages/api/src/DependencyInjection/Configuration.php"
      ]
    },
    {
      "description": "Inspected flat Page transfer and lock paths",
      "paths": [
        "packages/flat/src/Command/FlatFileSyncCommand.php",
        "packages/flat/src/Sync/PageSync.php",
        "packages/flat/src/Controller/Api/PageFileApiController.php",
        "packages/flat/src/Controller/FlatLockApiController.php",
        "packages/flat/src/Service/FlatLockManager.php",
        "packages/flat/src/EventSubscriber/FlatWebhookLockSubscriber.php",
        "packages/flat/src/Importer/PageImporter.php",
        "packages/flat/src/Service/FlatChangeDetector.php"
      ]
    },
    {
      "description": "Version capture comparison restoration and activity code",
      "paths": [
        "packages/version/src/"
      ]
    },
    {
      "description": "Inspected conversation forms moderation API and rendering",
      "paths": [
        "packages/conversation/src/"
      ]
    },
    {
      "description": "Snippet persistence API administration and resolution",
      "paths": [
        "packages/snippet/src/"
      ]
    },
    {
      "description": "Template source administration and filesystem paths",
      "paths": [
        "packages/template-editor/src/"
      ]
    },
    {
      "description": "Static rendering cache coordination and entry points",
      "paths": [
        "packages/static-generator/src/"
      ]
    },
    {
      "description": "Scheduled publication and editorial clock code",
      "paths": [
        "packages/core/src/Command/CronCommand.php",
        "packages/core/src/Scheduler/",
        "packages/core/src/Service/EditorialTimezone.php"
      ]
    },
    {
      "description": "Inspected search index and invalidation paths",
      "paths": [
        "packages/search/src/"
      ]
    },
    {
      "description": "Scan coordination entry points and result aggregation",
      "paths": [
        "packages/page-scanner/src/Controller/",
        "packages/page-scanner/src/Command/PageScannerCommand.php"
      ]
    },
    {
      "description": "Inspected media storage naming licensing and usage maintenance",
      "paths": [
        "packages/core/src/EventListener/MediaStorageListener.php",
        "packages/core/src/EventListener/MediaNamingListener.php",
        "packages/core/src/EventListener/MediaLicenseSeedListener.php",
        "packages/core/src/EventListener/MediaLicenseStateListener.php",
        "packages/core/src/EventListener/MediaUsageListener.php",
        "packages/core/src/Image/ImageRotator.php"
      ]
    },
    {
      "description": "Supported account and deletion operator commands",
      "paths": [
        "packages/core/src/Command/UserCreateCommand.php",
        "packages/core/src/Command/UserDeleteCommand.php",
        "packages/core/src/Command/UserTokenCommand.php",
        "packages/core/src/Command/DeletePageCommand.php"
      ]
    }
  ],
  "exclusions": [
    {
      "description": "Build release CI and development fixture infrastructure",
      "paths": [
        ".github/",
        "packages/dev-app/"
      ]
    }
  ],
  "unmapped": [
    {
      "description": "Campaign contact consent delivery automation and tracking code",
      "paths": [
        "packages/newsletter/src/"
      ]
    },
    {
      "description": "Quiz and repurposing lifecycle code",
      "paths": [
        "packages/quiz/src/",
        "packages/repurpose/src/"
      ]
    },
    {
      "description": "Supported agent contracts and delegated authority",
      "paths": [
        "packages/ai-skills/"
      ]
    },
    {
      "description": "Remaining specialized editor image selection and client helper code",
      "paths": [
        "packages/admin-block-editor/src/",
        "packages/admin-monaco-editor/",
        "packages/advanced-main-image/src/",
        "packages/js-helper/"
      ]
    },
    {
      "description": "Link maintenance and Page notification lifecycles",
      "paths": [
        "packages/link-improver/src/",
        "packages/page-update-notifier/src/"
      ]
    },
    {
      "description": "Remaining non-Page flat synchronization snapshots watching Git and administrative contracts",
      "paths": [
        "packages/flat/src/"
      ]
    },
    {
      "description": "Remaining installation cleanup and maintenance contracts",
      "paths": [
        "packages/core/src/Command/",
        "packages/installer/",
        "packages/new/"
      ]
    },
    {
      "description": "Remaining rendering filters and extension vocabulary",
      "paths": [
        "packages/core/src/Component/",
        "packages/core/src/Twig/"
      ]
    },
    {
      "description": "Detailed scanner checkers and independent link graph contracts",
      "paths": [
        "packages/page-scanner/src/"
      ]
    },
    {
      "description": "Complete media picker and parent-save hand-off code",
      "paths": [
        "packages/admin/src/Resources/assets/",
        "packages/admin/src/Controller/MediaCrudController.php"
      ]
    },
    {
      "description": "Complete impersonation and configured-role downstream authority",
      "paths": [
        "packages/core/src/Resources/config/packages/security.php",
        "packages/admin/src/Controller/UserCrudController.php"
      ]
    }
  ],
  "limitations": [
    {
      "description": "Framework hand-offs and exceptional restore deletion or storage effects not established beyond inspected handlers",
      "paths": [
        "packages/admin/src/Controller/",
        "packages/version/src/VersionController.php",
        "packages/core/src/EventListener/MediaStorageListener.php",
        "packages/template-editor/src/Element.php"
      ]
    },
    {
      "description": "Referenced-profile deletion consequences not fully traced",
      "paths": [
        "packages/core/src/Entity/",
        "packages/core/src/Command/UserDeleteCommand.php"
      ]
    },
    {
      "description": "Queue durability and outbound notification transport behavior not established by dispatch handlers",
      "paths": [
        "packages/core/src/BackgroundTask/",
        "packages/conversation/src/"
      ]
    },
    {
      "description": "Deployed serving CDN behavior and custom site overrides not established by generator code",
      "paths": [
        "packages/static-generator/src/",
        "packages/core/src/Controller/"
      ]
    }
  ]
}
---

# Coverage


