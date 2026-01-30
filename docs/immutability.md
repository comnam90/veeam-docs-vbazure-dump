---
title: "Immutability"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/immutability.html"
last_updated: "12/16/2025"
product_version: "8.0.1.202"
---

# Immutability


Veeam Backup for Microsoft Azure allows you to protect VM, SQL, Cosmos DB for PostgreSQL, Cosmos DB for MongoDB and virtual network configuration data stored in backup repositories from deletion by making the data temporarily immutable. To do that, Veeam Backup for Microsoft Azure uses [Immutable storage for Azure Blob Storage](https://learn.microsoft.com/en-us/azure/storage/blobs/immutable-storage-overview) — once imposed, Immutable storage prevents objects from being deleted or overwritten for a specific immutability period. The immutability period is set based on the retention policy configured in the backup policy settings.

|  |
| --- |
| Note |
| To reduce the number of requests sent to immutable repositories during VM, SQL, Cosmos DB and virtual network configuration backup operations, Veeam Backup for Microsoft Azure leverages the [Block Generation mechanism](block_generation.md). |

Considerations and Limitations

Before you start creating immutable backups, keep in mind the following limitations:

* You cannot manually remove immutable data from immutable repositories using the Veeam Backup for Microsoft Azure Web UI, as described in sections [Removing VM Backups and Snapshots](removing_vm_backups_and_snapshots.md), [Removing SQL Backups](removing_sql_backups.md), [Removing Cosmos DB Backups](removing_cosmos_db_backups.md) and [Removing Virtual Network Configuration Backups](removing_vnet_backups.md) — until the immutability period is over.
* You can neither remove data from Microsoft Azure using any cloud service provider tools nor request the technical support department to do it for you — none of the protected objects can be overwritten or deleted by any user, including the Global Administrator in your Microsoft Entra ID.

How To Create Immutable Backups

To protect backups created with Veeam Backup for Microsoft Azure from deletion by making them temporarily immutable, perform the following steps:

1. [Add a backup repository with immutability enabled](repository_add_ui.md#enable_efs_indexing).
2. Create a backup policy and specify the repository with immutability enabled as the target location for image-level backups. For more information, see sections [Creating VM Backup Policies](vm_backup_create.md), [Creating SQL Backup Policies](sql_backup_create.md), [Creating Cosmos DB Backup Policies](cosmos_db_backup_create.md) and [Editing Virtual Network Configuration Backup Policy](vnet_backup_edit.md).


