---
title: "performing_disk_restore"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/performing_disk_restore.html"
last_updated: "11/1/2023"
product_version: "8.0.1.202"
---


In this article

In case a disaster strikes, you can restore corrupted virtual disks of an Azure VM from a cloud-native snapshot or image-level backup. Veeam Backup for Microsoft Azure allows you to restore virtual disks to the original location or to a new location.

Before You Begin

To restore a virtual disk from a backup that is stored in an archive repository, you must retrieve the archived data first. You can either retrieve the archived data manually before you begin the restore operation, or launch the data retrieval process right from the restore wizard. To learn how to retrieve data manually, see [Retrieving Data From Archive](retrieving_vm_data.md).

How to Perform Disk Restore

To restore virtual disks attached to a protected Azure VMs, do the following:

1. [Launch the Restore Disks wizard](disk_restore_wizard.md).
2. [Select a restore point](disk_restore_point.md).
3. [Select a service account](disk_restore_account.md).
4. [Choose a restore mode](disk_restore_mode.md).
5. [Specify data retrieval settings](disk_retrieve.md).
6. [Specify disk settings](disk_restore_disks.md).
7. [Specify a restore reason](disk_restore_reason.md).
8. [Finish working with the wizard](disk_restore_finish.md).

Page updated 11/1/2023

Page content applies to build 8.0.1.202
