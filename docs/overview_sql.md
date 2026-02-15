---
title: "Protecting Azure SQL Databases"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/overview_sql.html"
last_updated: "2/13/2026"
product_version: "8.0.1.202"
---

# Protecting Azure SQL Databases


To produce backups of Azure SQL databases, Veeam Backup for Microsoft Azure runs backup policies. A backup policy is a collection of settings that define the way backup operations are performed: what data to back up, where to store backups, when to start the backup process, and so on.

Veeam Backup for Microsoft Azure does not install agent software to back up Azure SQL data — it uses native Microsoft Azure capabilities instead. During every backup session, Veeam Backup for Microsoft Azure creates a BACPAC file for each Azure SQL database added to a backup policy. The BACPAC file is further used to create a backup of the Azure SQL database. For more information on how SQL backup works, see [SQL Backup](how_sql_backup_works.md).

How To Protect Azure SQL Databases

To create an Azure SQL backup policy, perform the following steps:

1. [Check limitations and prerequisites](limitations.md#backup).
2. [Specify service accounts to access Azure services and resources](service_accounts.md).
3. [[Optional] Add repositories to store backed-up data](repositories.md).
4. [[Optional] Configure worker instance settings to launch workers while processing Azure SQL data](workers.md).
5. [[Optional] Configure global retention settings for obsolete session records](configuring_global_retention.md).
6. [[Optional] Configure email notification settings for automated delivery of backup policy results and daily reports](configuring_notification_settings.md).
7. [Complete the Add Azure SQL Policy wizard](sql_backup_wizard.md).

Related Topics

[SQL Restore](sql_restore_hiw.md)


