---
title: "cosmos_db_restore_point_in_time"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/cosmos_db_restore_point_in_time.html"
last_updated: "9/11/2024"
product_version: "8.0.1.202"
---


In this article

In case a disaster strikes, you can restore an entire Cosmos DB account or its specific items from a timestamp. Veeam Backup for Microsoft Azure allows you to restore one Cosmos DB account at a time to a new location.

|  |
| --- |
| Important |
| Consider the following:   * Point-in-time restore is not available for Cosmos DB accounts that have the Deleting status. * Point-in-time restore is not available for Cosmos DB for PostgreSQL accounts that have either the Deleted, Stopped or Dropping status.   However, accounts with the Deleted status can still be restored if they have backups stored in repositories. To learn how to do that, see [Performing Restore From Repository](cosmos_db_restore_from_repository.md). |

How to Perform Cosmos DB Restore

To restore a Cosmos DB account, do the following:

1. [Launch the Cosmos DB Restore wizard](cosmos_db_restore_point_in_time_wizard.md).
2. [Select a restore point](cosmos_db_restore_point_in_time_point.md).
3. [Select a service account](cosmos_db_restore_point_in_time_service_account.md).
4. [Configure restore settings](cosmos_db_restore_point_in_time_settings.md).
5. [Specify a restore reason](cosmos_db_restore_point_in_time_reason.md).
6. [Finish working with the wizard](cosmos_db_restore_point_in_time_finish.md).

Page updated 9/11/2024

Page content applies to build 8.0.1.202
