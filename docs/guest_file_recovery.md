---
title: "guest_file_recovery"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/guest_file_recovery.html"
last_updated: "12/23/2025"
product_version: "8.0.1.202"
---


In this article

Veeam Backup & Replication allows you to use image-level backups to restore files and folders of various VM guest OS file systems from the Veeam Backup & Replication console. For more information, see the Veeam Backup & Replication User Guide, section [Guest OS File Restore](https://helpcenter.veeam.com/docs/vbr/userguide/guest_file_recovery.html?ver=13).

|  |
| --- |
| Important |
| * Guest OS file restore cannot be performed using backups that are stored in [Veeam Data Cloud storage vaults](vdc_vaults.md). To perform this operation, use backups that are stored in standard backup repositories for which you have specified Microsoft Azure storage account credentials. To learn how to specify credentials for repositories, see sections [Creating New Repositories](repository_console_storage_account.md) and [Connecting to Existing Appliances](adding_appliance_repository.md). * Before you start the restore operation, check the limitations and prerequisites described in the Veeam Backup & Replication User Guide, section [Considerations and Limitations](https://helpcenter.veeam.com/docs/vbr/userguide/vbr_flr_considerations_common.html?ver=13). |

To restore guest OS files and folders, do the following:

1. In the Veeam Backup & Replication console, open the Home view.
2. Navigate to Backups > External Repository.
3. Expand the backup policy that protects an Azure VM whose files and folders you want to restore, select the necessary VM and click Restore Guest Files on the ribbon.

1. Complete the File Level Restore wizard as described in the Veeam Backup & Replication User Guide, section [Recovering Guest OS Files Using Console](https://helpcenter.veeam.com/docs/vbr/userguide/performing_guest_restore.html?ver=13).

|  |
| --- |
| Tips |
| * If the file system whose files and folders you want to restore is not included in the [list of supported systems](https://helpcenter.veeam.com/docs/vbr/userguide/platform_support.html?ver=13#guest-os-file-restore), you can restore them using the Instant Disk Recovery technology. For more information, see the Veeam Backup & Replication User Guide, section [Restore from Other File Systems](https://helpcenter.veeam.com/docs/vbr/userguide/guest_restore_other.html?ver=13). * You can also perform file-level recovery using the Veeam Backup for Microsoft Azure Web UI. For more information, see [Performing File-Level Recovery](performing_flr.md). |

[![Restore guest OS files](images/restore_guest_os_files.webp)](images/restore_guest_os_files.webp "Restore guest OS files")

Page updated 12/23/2025

Page content applies to build 8.0.1.202
