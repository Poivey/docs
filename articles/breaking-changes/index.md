---
toc: true
title: Auth0 Breaking Changes
description: List of all the changes made on Auth0 platform that might affect customers
topics:
  - migrations
  - deprecations
contentType:
  - concept
  - reference
useCase:
  - migrate
---

# Breaking Changes

Occasionally, Auth0 engineers must make breaking changes to the Auth0 platform, primarily for security reasons. If a vulnerability or other problem in the platform is not up to our high standards of security, we work to correct the issue.

Sometimes a correction will cause a breaking change to customer's applications. Depending on the severity of the issue, we may have to make the change immediately.

For changes that do not require immediate changes, we often allow a grace period to allow you time to update your applications.

## Migration process

The migration process is outlined below:

1. We update the platform and add a new migration option for existing customers, allowing a grace period for opt-in. New customers are always automatically enrolled in all migrations.
2. After a certain period, the migration is enabled for all customers. This grace period varies based on the severity and impact of the breaking change.

During the grace period, customers are informed via dashboard notifications and emails to tenant administrators. You will continue to receive emails until the migration has been enabled on each tenant you administer.

If you need help with the migration, create a ticket in our [Support Center](${env.DOMAIN_URL_SUPPORT}).

## Active migrations

Migrations of type **Deprecation** require action by the features **Removal Date.** See [Deprecations](/deprecations) for more information.

| Description | Type | Guide |
| - | - | - |
| User Search v2 | Deprecation | [User Search v2 -> v3 migration guide](/users/search/v3/migrate-search-v2-v3) |
| Tenant Logs Search v2 | Deprecation | [Tenant Logs Search v2 -> v3 migration guide](/logs/migrate-logs-v2-v3) |
| Node v4 Extensibility Runtime | Deprecation | [Extensibility and Node.js v8](/migrations/guides/extensibility-node8) |
| Clickjacking Protection for classic Universal Login Experience | Product Enhancement | [Enable clickjacking protection](/migrations/guides/clickjacking-protection) |
| Google Cloud Messaging to Firebase Cloud Messaging Migration | 3rd Party Change | Existing applications will keep working but if you want to migrate, you can find instructions [here](/migrations/guides/google_cloud_messaging) |
| Facebook Login and Graph API | 3rd Party Change | [Changes to Facebook Login and Graph API](/migrations/guides/facebook-graph-api-deprecation) |
| LinkedIn API v2 | 3rd Party Change | [Migration to LinkedIn API V2](/migrations/guides/linkedin-api-deprecation) |
| Allow ID Tokens for Management API v2 Authentication | Planned Deprecation | [Management API and ID Tokens](/migrations/guides/calling-api-with-idtokens) |
| Legacy `oauth/ro` Endpoint | Planned Deprecation | [Migration Guide for Resource Owner Password Credentials Exchange](/migrations/guides/migration-oauthro-oauthtoken) |
| Legacy Delegation Endpoint | Planned Deprecation | See [Planned Deprecations](/deprecations/planned-deprecations) for more info |
| Legacy User Profile | Planned Deprecation | See [Planned Deprecations](/deprecations/planned-deprecations) for more info |

For migrations that have already been enabled for all customers, see [Past Migrations](/migrations/past-migrations).

If you have any questions, reach out in our [Support Center](${env.DOMAIN_URL_SUPPORT}).