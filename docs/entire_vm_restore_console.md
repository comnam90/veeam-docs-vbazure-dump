---
title: "entire_vm_restore_console"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/entire_vm_restore_console.html"
last_updated: "8/19/2025"
product_version: "8.0.1.202"
---


In this article

In case a disaster strikes, you can restore entire Azure VM from a cloud-native snapshot or an image-level backup. Veeam Backup & Replication allows you to restore one or more Azure VMs at a time, to the original location or to a new location.

How Instance Restore Works

To restore Azure VMs from cloud-native snapshots, Veeam Backup & Replication uses [native Azure capabilities](https://learn.microsoft.com/en-us/azure/virtual-machines/snapshot-copy-managed-disk?tabs=portal). To restore VMs from image-level backups, Veeam Backup & Replication uses different algorithms depending on whether a backup appliance is added to the backup infrastructure:

* If a backup appliance is connected to the backup server, Veeam Backup & Replication uses the restore algorithm described in section [Performing Entire VM Restore](entire_vm_restore_ui.md).
* If a backup appliance is not connected to the backup server, Veeam Backup & Replication uses the restore algorithm described in the Veeam Backup & Replication User Guide, section [How Restore to Microsoft Azure Works](https://helpcenter.veeam.com/docs/vbr/userguide/restore_azure_hiw.html?ver=13).

How to Perform VM Restore

To restore an entire VM, do the following:

1. [Launch the Restore to Azure wizard](vm_restore_console_wizard.md).
2. [Select a restore point](vm_restore_console_point.md).
3. [Choose a restore mode](vm_restore_console_mode.md).
4. [Specify an Azure subscription and region](vm_restore_console_subscription.md).
5. [Specify a new VM name and resource group](vm_restore_console_name.md).
6. [Specify VM configuration settings](vm_restore_console_zone.md).
7. [Specify a VM size](vm_restore_console_size.md).
8. [Configure network and security group settings](vm_restore_console_network.md).
9. [Specify a restore reason](vm_restore_console_reason.md).
10. [Finish working with the wizard](vm_restore_console_finish.md).

Page updated 8/19/2025

Page content applies to build 8.0.1.202
