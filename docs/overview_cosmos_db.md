---
title: "overview_cosmos_db"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/overview_cosmos_db.html"
last_updated: "6/10/2025"
product_version: "8.0.1.202"
---


In this article

To produce backups of Cosmos DB accounts, Veeam Backup for Microsoft Azure runs backup policies. A backup policy is a collection of settings that define the way backup operations are performed: what data to back up, where to store backups, when to start the backup process, and so on.

By default, Veeam Backup for Microsoft Azure does not install agent software to back up Cosmos DB account data — it uses native Microsoft Azure capabilities instead. Every time Veeam Backup for Microsoft Azure synchronizes data between Microsoft Azure and the configuration database, it creates a database record for each Cosmos DB account added to a backup policy. You can also instruct Veeam Backup for Microsoft Azure to create backups of the processed Cosmos DB for PostgreSQL clusters and Cosmos DB for MongoDB accounts. For more information on how Cosmos DB backup works, see [Cosmos DB Backup](how_cosmos_db_backup_works.md).

How To Protect Cosmos DB Accounts

To create a Cosmos DB backup policy, perform the following steps:

1. [Check limitations and prerequisites](limitations.md#backup).
2. [Specify service accounts to access Azure services and resources](service_accounts.md).
3. [[Optional] Add backup repositories to store backed-up data](repositories.md).
4. [[Optional] Configure worker instance settings to launch workers while processing Cosmos DB data](workers.md).
5. [[Optional] Configure global retention settings for obsolete session records](configuring_global_retention_settings.md#sessions).
6. [[Optional] Configure email notification settings for automated delivery of backup policy results and daily reports](configuring_notification_settings.md).
7. [Complete the Add Cosmos DB Policy wizard](cosmos_db_backup_wizard.md).

Related Topics

[Cosmos DB Restore](cosmos_db_restore_hiw.md)

Page updated 6/10/2025

Page content applies to build 8.0.1.202
