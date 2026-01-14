---
title: "performing_flr"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/performing_flr.html"
last_updated: "8/19/2025"
product_version: "8.0.1.202"
---


In this article

In case a disaster strikes, you can recover corrupted or missing files of an Azure VM from a cloud-native snapshot or image-level backup. Veeam Backup for Microsoft Azure allows you to download the necessary files and folders to a local machine, or restore the files and folders of the source Azure VM to the original location, using the [File-level recovery browser](flr_download.md).

|  |
| --- |
| Important |
| * File-level recovery is supported from FAT, FAT32, NTFS, ext2, ext3, ext4, XFS, Btrfs file systems only. For Microsoft Windows systems, file-level recovery is supported for basic volumes only.   If you want to recover files from file systems that are not supported by Veeam Backup for Microsoft Azure, you can add a backup repository that contains backups of Azure VMs to the backup infrastructure as an external repository, and perform the file-level recovery operation as described in the [Veeam Backup & Replication User Guide](https://helpcenter.veeam.com/docs/vbr/userguide/external_repository.html?ver=13).   * File-level recovery to the original location is supported only for Windows-based Azure VMs running Windows Server version 2016 (or later) and Windows version 10 (or later), and for Linux-based Azure VMs using the [systemd init system](https://learn.microsoft.com/en-us/windows/wsl/systemd). * File-level recovery of Azure VMs with the [Azure Disk Encryption option](https://learn.microsoft.com/en-us/azure/virtual-machines/disk-encryption-overview) enabled is not supported in the current Veeam Backup for Microsoft Azure version. * File-level recovery from virtual disks with Windows-native [Data Deduplication](https://learn.microsoft.com/en-us/windows-server/storage/data-deduplication/overview) enabled is not supported. To work around the issue, you can restore entire virtual disks, and then attach these disks to an Azure VM with the deduplication feature enabled. To learn how to restore entire virtual disks, see [Performing Disk Restore](performing_disk_restore.md). * File-level recovery of [Arm-based Azure VMs](https://learn.microsoft.com/en-us/windows/arm/create-arm-vm) to the original location is not supported. |

To recover files and folders of a protected Azure VM, do the following:

1. [Launch the File-Level Recovery wizard](flr_wizard.md).
2. [Select a restore point](flr_restore_point.md).
3. [Configure restore settings](flr_restore_settings.md).
4. [Specify a restore reason](flr_reason.md).
5. [Finish working with the wizard — start a recovery session](flr_restore_session.md).
6. [Choose files and folders to recover](flr_download.md).
7. [Stop the recovery session](flr_stop_session.md).

|  |
| --- |
| Important |
| To recover files and folders of an Azure VM from a backup that is stored in an archive backup repository, you must retrieve the archived data manually before you begin the file-level recovery operation. To learn how to do that, see [Retrieving Data from Archive](retrieving_vm_data.md). |

Page updated 8/19/2025

Page content applies to build 8.0.1.202
