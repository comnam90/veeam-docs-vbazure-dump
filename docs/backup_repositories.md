---
title: "Backup Repositories"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/backup_repositories.html"
last_updated: "11/28/2025"
product_version: "8.0.1.202"
---

# Backup Repositories


A backup repository is a folder in a blob container where Veeam Backup for Microsoft Azure stores image-level backups of Azure VMs, backups of Azure SQL databases, backups of Cosmos DB for PostgreSQL and Cosmos DB for MongoDB accounts, and backup copies of virtual network configurations.

To communicate with backup repositories, Veeam Backup for Microsoft Azure uses Veeam Data Mover — a service that runs on [worker instances](worker_instances.md) and that is responsible for data processing and transfer. When a backup policy addresses a backup repository, Veeam Data Mover establishes a connection with the repository to enable data transfer. To learn how Veeam Backup for Microsoft Azure communicates with backup repositories, see [Managing Repositories](repositories.md).

|  |
| --- |
| Important |
| Backup files are stored in backup repositories in the native Veeam format and must not be modified manually or by 3rd party tools. Otherwise, Veeam Backup for Microsoft Azure may fail to restore the backed-up data. |

Encryption on Backup Repositories

For enhanced data security, Veeam Backup for Microsoft Azure allows you to enable encryption at the repository level. Veeam Backup for Microsoft Azure encrypts backup files stored in backup repositories the same way as Veeam Backup & Replication encrypts backup files stored in backup repositories. To learn what algorithms Veeam Backup & Replication uses to encrypt backup files, see the Veeam Backup & Replication User Guide, section [Data Encryption](https://helpcenter.veeam.com/docs/vbr/userguide/data_encryption.html?ver=13). To learn how to enable encryption at the repository level, see [Adding Backup Repositories](repository_ui_encryption.md).

Limitations for Repositories

To use a blob container as a target location for backups, you must connect to an Azure storage account in which this blob container resides, as described in section [Adding Backup Repositories Using Web UI](repository_ui_settings.md).

Veeam Backup for Microsoft Azure supports the following types of Azure storage accounts:

| Storage Account Type | Supported Performance Tiers | Supported Access Tiers |
| --- | --- | --- |
| General-purpose V2 | Standard | Hot, Cool, Archive |
| BlobStorage | Standard | Hot, Cool, Archive |

|  |
| --- |
| Important |
| Consider the following limitations for storage accounts:   * Veeam Backup for Microsoft Azure does not support creation of backup repositories in storage accounts with the [blob soft delete](https://docs.microsoft.com/en-us/azure/storage/blobs/soft-delete-blob-overview#recommended-data-protection-configuration) option enabled. * Veeam Backup for Microsoft Azure does not support creation of backup repositories in the Cold access tier. For more information on access tiers for blob data, see [Microsoft Docs](https://learn.microsoft.com/en-us/azure/storage/blobs/access-tiers-overview).  * Due to Microsoft Azure limitations, Veeam Backup for Microsoft Azure does not support creation of archive repositories in storage accounts with the [Zone-redundant storage](https://learn.microsoft.com/en-us/azure/storage/common/storage-redundancy#zone-redundant-storage) (ZRS), [Geo-zone-redundant storage](https://learn.microsoft.com/en-us/azure/storage/common/storage-redundancy#geo-zone-redundant-storage) (GZRS) or [Read-access geo-zone-redundant storage](https://learn.microsoft.com/en-us/azure/storage/common/storage-redundancy#read-access-to-data-in-the-secondary-region) (RA-GZRS) redundancy option enabled. For more information, see [Microsoft Docs](https://learn.microsoft.com/en-us/azure/storage/blobs/access-tiers-overview#archive-access-tier). |


