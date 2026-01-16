---
title: "sql_backup_retention"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/sql_backup_retention.html"
last_updated: "12/9/2025"
product_version: "8.0.1.202"
---


In this article

For image-level backups, Veeam Backup for Microsoft Azure retains restore points for the number of days defined in backup scheduling settings as described in section [Creating SQL Backup Policies](sql_backup_policy_schedule.md).

To track and remove outdated restore points from a backup chain, Veeam Backup for Microsoft Azure performs the following actions once a day:

1. Veeam Backup for Microsoft Azure checks the configuration database to detect blob containers that contain outdated restore points.
2. If an outdated restore point exists in a blob container, Veeam Backup for Microsoft Azure deploys a worker instance in an Azure region in which the container with backed-up data resides.
3. Veeam Backup for Microsoft Azure transforms the backup chain in the following way:

1. Veeam Backup for Microsoft Azure rebuilds the full backup to include data of the incremental backup that follows the full backup. To do that, Veeam Backup for Microsoft Azure injects into the full backup data blocks from the earliest incremental backup in the chain. This way, the full backup ‘moves’ forward in the backup chain.

![SQL Backup Retention](images/backup_retention_injecting_blocks.webp)

1. Veeam Backup for Microsoft Azure removes the earliest incremental backup from the chain as redundant — this data has already been injected into the full backup.

![SQL Backup Retention](images/backup_retention_removing_data.webp)

1. Veeam Backup for Microsoft Azure repeats step 2 for all other outdated restore points found in the backup chain until all the restore points are removed. As data from multiple restore points is injected into the rebuilt full backup, Veeam Backup for Microsoft Azure ensures that the backup chain is not broken and that you will be able to recover your data when needed.

![SQL Backup Retention](images/backup_retention_multiple_points.webp)

Related Topics

[Retention Policy for Archived Backups](sql_archive_backup_retention.md)

Page updated 12/9/2025

Page content applies to build 8.0.1.202
