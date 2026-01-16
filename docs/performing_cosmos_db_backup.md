---
title: "performing_cosmos_db_backup"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/performing_cosmos_db_backup.html"
last_updated: "9/9/2025"
product_version: "8.0.1.202"
---


In this article

|  |
| --- |
| Important |
| Cosmos DB backup is available only for backup appliances managed by a Veeam Backup & Replication server. To unlock the full functionality, you must [install Veeam Plug-in for Microsoft Azure on the server](deploying_vb.md) and [add your appliances](adding_appliance_console.md) to the backup infrastructure. |

One backup policy can be used to process one or more Cosmos DB accounts within one Microsoft Entra tenant. The scope of data that you can protect in a tenant is limited by permissions of a service account that is specified in the backup policy settings.

Before you create an Cosmos DB backup policy, check the following prerequisites:

* If you plan to enable backup to repository, backup infrastructure components that will take part in the backup process must be added to the backup infrastructure and configured properly. These include [repositories](repositories.md) and [worker instances](workers.md).
* If you plan to receive email notifications on backup policy results, configure email notification settings first. For more information, see [Configuring Global Notification Settings](configuring_notification_settings.md).

To schedule data protection tasks to run automatically, [create backup policies](cosmos_db_backup_create.md). For each protected Cosmos DB for PostgreSQL or Cosmos DB for MongoDB account, you can also [take a backup to a repository manually](creating_cosmos_db_backups_manually.md) when needed.

|  |
| --- |
| Important |
| Consider the following:   * Veeam Backup for Microsoft Azure allows you to protect only Cosmos DB accounts created using the following APIs: NoSQL, MongoDB RU-based, Apache Gremlin, Table and PostgreSQL. * Veeam Backup for Microsoft Azure does not support protecting Cosmos DB accounts that have [periodic backup](https://learn.microsoft.com/en-us/azure/cosmos-db/periodic-backup-restore-introduction) or [multi-region writes](https://learn.microsoft.com/en-us/azure/cosmos-db/how-to-manage-database-account#configure-multiple-write-regions) enabled. |

Page updated 9/9/2025

Page content applies to build 8.0.1.202
