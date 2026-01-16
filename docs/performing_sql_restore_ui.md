---
title: "performing_sql_restore_ui"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/performing_sql_restore_ui.html"
last_updated: "4/29/2024"
product_version: "8.0.1.202"
---


In this article

In case a disaster strikes, you can restore an entire Azure SQL database from an image-level backup. Veeam Backup for Microsoft Azure allows you to restore one or more databases at a time, to the original location or to a new location.

|  |
| --- |
| Important |
| Within one restore session, you can restore only those Azure SQL databases that belong to the same SQL Server. |

Before You Begin

To restore an Azure SQL database from a backup that is stored in an archive repository, you must retrieve the archived data first. You can either retrieve the archived data manually before you begin the restore operation, or launch the data retrieval process right from the restore wizard. To learn how to retrieve data manually, see [Retrieving Data From Archive](retrieving_sql_data.md).

How to Perform SQL Restore

To restore an Azure SQL database, do the following:

1. [Launch the SQL Database restore wizard](sql_restore_ui_wizard.md).
2. [Select a restore point](sql_restore_ui_point.md).
3. [Select a service account](sql_restore_ui_service_account.md).
4. [Choose a restore mode](sql_restore_ui_mode.md).
5. [Select an Azure SQL account](sql_restore_ui_sql_account.md).
6. [Specify data retrieval settings](sql_restore_ui_retrieve.md).
7. [Configure restore settings](sql_restore_ui_settings.md).
8. [Specify a restore reason](sql_restore_ui_reason.md).
9. [Review summary information](sql_restore_ui_finish.md).

Page updated 4/29/2024

Page content applies to build 8.0.1.202
