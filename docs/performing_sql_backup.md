---
title: "Performing SQL Backup"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/performing_sql_backup.html"
last_updated: "8/20/2025"
product_version: "8.0.1.202"
---

# Performing SQL Backup


One backup policy can be used to process one or more Azure SQL databases within one Microsoft Entra tenant. The scope of data that you can protect in a tenant is limited by permissions of a service account that is specified in the backup policy settings.

Before you create an Azure SQL backup policy, check the following prerequisites:

* If you plan to create backups of Azure SQL databases, backup infrastructure components that will take part in the backup process must be added to the backup infrastructure and configured properly. These include [repositories](repositories.md) and [worker instances](workers.md).
* If you plan to receive email notifications on backup policy results, configure email notification settings first. For more information, see [Configuring Global Notification Settings](configuring_notification_settings.md).

To schedule data protection tasks to run automatically, [create backup policies](sql_backup_create.md). For each protected Azure SQL database, you can also [take a backup manually](creating_sql_backups_manually.md) when needed.

|  |
| --- |
| Important |
| Veeam Backup for Microsoft Azure does not allow you to protect databases hosted by Azure Arc-enabled SQL Managed Instances and SQL Servers on Azure Arc-enabled servers. |


