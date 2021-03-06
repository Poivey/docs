---
title: Bulk User Import Database Schema and Example 
description: How to perform bulk user imports with the Management API.
topics:
  - users
  - user-management
  - migrations
  - bulk-imports
contentType:
  - reference
useCase:
  - manage-users
  - migrate
---
# Bulk User Import Database Schema and Example

::: note
For a list of user profile fields that can be imported, see [User Profile Attributes](/users/references/user-profile-structure#user-profile-attributes).
:::

The users file must have an array with the users' information in JSON format.

The following [JSON schema](http://json-schema.org) describes valid users:

```json
{
    "type": "object",
    "properties": {
        "email": {
            "type": "string",
            "description": "The user's email address.",
            "format": "email"
        },
        "email_verified": {
            "type": "boolean",
            "default": false,
            "description": "Indicates whether the user has verified their email address."
        },
        "user_id": {
            "type": "string",
            "description": "The user's unique identifier. This will be prepended by the connection strategy."
        },
        "username": {
            "type": "string",
            "description": "The user's username."
        },
        "given_name": {
            "type": "string",
            "description": "The user's given name."
        },
        "family_name": {
            "type": "string",
            "description": "The user's family name."
        },
        "name": {
            "type": "string",
            "description": "The user's full name."
        },
        "nickname": {
            "type": "string",
            "description": "The user's nickname."
        },
        "picture": {
          "type": "string",
          "description": "URL pointing to the user's profile picture."
        },
        "blocked": {
            "type": "boolean",
            "description": "Indicates whether the user has been blocked."
        },
        "password_hash": {
            "type": "string",
            "description":"Hashed password for the user. Passwords should be hashed using bcrypt $2a$ or $2b$ and have 10 saltRounds."
        },
        "app_metadata": {
            "type": "object",
            "description": "Data related to the user that does affect the application's core functionality."
        },
        "user_metadata": {
            "type": "object",
            "description": "Data related to the user that does not affect the application's core functionality."
        }
    },
    "required": ["email"],
    "additionalProperties": false
}
```

::: note
The file size limit for a bulk import is 500KB. You will need to start multiple imports if your data exceeds this size.
:::

## Keep reading

* [User Migration Overview](/users/concepts/overview-user-migration)
* [Configure Automatic Migration](/users/guides/configure-automatic-migration)
* [Bulk User Imports](/users/guides/bulk-user-imports)
* [User Import/Export Extension](/extensions/user-import-export)
* [User Migration Scenarios](/users/references/user-migration-scenarios)
* [Migrating Stormpath Users to Auth0 Demo](https://github.com/auth0-blog/migrate-stormpath-users-to-auth0)
