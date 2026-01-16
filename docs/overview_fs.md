---
title: "overview_fs"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/overview_fs.html"
last_updated: "9/19/2024"
product_version: "8.0.1.202"
---


In this article

To produce snapshots of Azure file shares, Veeam Backup for Microsoft Azure runs backup policies. A backup policy is a collection of settings that define the way snapshots are created: what data to protect, when to start the snapshot creation process, and so on.

Veeam Backup for Microsoft Azure does not install agent software to back up Azure Files data — it uses native Microsoft Azure capabilities instead. During every backup session, Veeam Backup for Microsoft Azure creates a cloud-native snapshot for each Azure file share added to a backup policy. For more information on how Azure Files backup works, see [Azure Files Backup](how_fs_backup_works.md).

How To Protect Azure File Shares

To create an Azure Files backup policy, perform the following steps:

1. [Check limitations and prerequisites](limitations.md#backup).
2. [Specify service accounts to access Azure services and resources](service_accounts.md).
3. [[Optional] Configure worker instance settings to launch workers while processing Azure Files data](workers.md).
4. [[Optional] Configure global retention settings for obsolete snapshots and session records](configuring_global_retention_settings.md).
5. [[Optional] Configure email notification settings for automated delivery of backup policy results and daily reports](configuring_notification_settings.md).
6. [Complete the Add Azure Files Policy wizard](fs_backup_wizard.md).

Related Topics

[File Share Restore](fs_restore_hiw.md)

Page updated 9/19/2024

Page content applies to build 8.0.1.202
