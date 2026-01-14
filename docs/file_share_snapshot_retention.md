---
title: "file_share_snapshot_retention"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/file_share_snapshot_retention.html"
last_updated: "12/9/2025"
product_version: "8.0.1.202"
---


In this article

For cloud-native snapshots, Veeam Backup for Microsoft Azure retains the number of latest restore points defined in backup scheduling settings as described in section [Creating Azure Files Backup Policies](fs_backup_policy_schedule.md).

During every successful backup session, Veeam Backup for Microsoft Azure creates a new restore point. If Veeam Backup for Microsoft Azure detects that the number of restore points in the snapshot chain exceeds the retention limit, it removes the earliest restore point from the chain. For more information on the snapshot deletion process, see [Microsoft Docs](https://docs.azure.cn/en-us/storage/files/storage-files-prevent-file-share-deletion?tabs=azure-portal).

[![File Share Snapshot Retention](images/snapshot_retention.webp)](images/snapshot_retention.webp)

|  |
| --- |
| Note |
| Consider that Veeam Backup for Microsoft Azure does not apply retention policy settings to cloud-native snapshots created manually. To learn how to remove these snapshots, see [Managing Azure Files Data](removing_fs_manual_snaphots.md). |

Page updated 12/9/2025

Page content applies to build 8.0.1.202
