---
title: "Azure Files Permissions"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/fs_permissions.html"
last_updated: "3/27/2025"
product_version: "8.0.1.202"
---

# Azure Files Permissions


To allow Veeam Backup for Microsoft Azure to protect Azure file shares, the service account that will be used for backup and restore operations with the file shares must have the following permissions.

Azure Files Snapshot and Restore Permissions

|  |
| --- |
| {  "permissions": [         {         "actions": [                 "Microsoft.Authorization/roleAssignments/read",                 "Microsoft.Insights/eventtypes/values/Read",                 "Microsoft.Resources/subscriptions/resourceGroups/read",                 "Microsoft.Storage/storageAccounts/listKeys/action",                 "Microsoft.Storage/storageAccounts/read"         ],         "notActions": [],         "dataActions": [],         "notDataActions": []         }     ]  } |


