---
title: "permissions_changelog"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/permissions_changelog.html"
last_updated: "9/10/2025"
product_version: "8.0.1.202"
---


In this article

This section describes the latest changes in service account permissions required for Veeam Backup for Microsoft Azure to perform operations.

When you update Veeam Backup for Microsoft Azure version 8 to version 8.1, consider that service accounts must be assigned additional permissions:

* For Veeam Backup for Microsoft Azure to be able to automatically create private endpoints when protecting Azure SQL databases and Cosmos DB accounts that have public access disabled, service accounts must be additionally assigned the following permissions:

|  |
| --- |
| "Microsoft.DBforPostgreSQL/serverGroupsv2/privateEndpointConnectionsApproval/action",  "Microsoft.DBforPostgreSQL/serverGroupsv2/privateEndpointConnections/read",  "Microsoft.DBforPostgreSQL/serverGroupsv2/privateEndpointConnections/write",  "Microsoft.DocumentDB/databaseAccounts/PrivateEndpointConnectionsApproval/action",  "Microsoft.DocumentDB/databaseAccounts/privateEndpointConnections/read",  "Microsoft.DocumentDB/databaseAccounts/privateEndpointConnections/write",  "Microsoft.Sql/ManagedInstances/privateEndpointConnections/read",  "Microsoft.Sql/ManagedInstances/privateEndpointConnections/write",  "Microsoft.Sql/servers/privateEndpointConnections/read",  "Microsoft.Sql/servers/privateEndpointConnections/write",  "Microsoft.Sql/servers/PrivateEndpointConnectionsApproval/action" |

* For Veeam Backup for Microsoft Azure to be able to manage Azure storage accounts that have [Shared Key authorization disabled](https://learn.microsoft.com/en-us/azure/storage/common/shared-key-authorization-prevent?tabs=portal), service accounts must be additionally assigned the following permission:

|  |
| --- |
| "Microsoft.Storage/storageAccounts/blobServices/generateUserDelegationKey/action" |

* For Veeam Backup for Microsoft Azure to be able to delete temporary containers in Veeam storage accounts when performing file-level recovery to the original location, service accounts must be additionally assigned the following permission:

|  |
| --- |
| "Microsoft.Storage/storageAccounts/blobServices/containers/delete" |

* For Veeam Backup for Microsoft Azure to be able to manage Azure storage accounts that have [Shared Key authorization disabled](https://learn.microsoft.com/en-us/azure/storage/common/shared-key-authorization-prevent?tabs=portal), service accounts must be additionally assigned the following dataActions:

|  |
| --- |
| "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/add/action",  "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/delete",  "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read",  "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" |

|  |
| --- |
| Note |
| The "Microsoft.DocumentDB/databaseAccounts/restore/action" permission is no longer required for Veeam Backup for Microsoft Azure to perform any operations as it has been retired in Microsoft Azure. |

Page updated 9/10/2025

Page content applies to build 8.0.1.202
