---
title: "vm_restore_entire_hiw"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/vm_restore_entire_hiw.html"
last_updated: "11/28/2025"
product_version: "8.0.1.202"
---


In this article

To restore an Azure VM from a cloud-native snapshot, Veeam Backup for Microsoft Azure uses [native Microsoft Azure capabilities](https://docs.microsoft.com/en-us/azure/backup/backup-azure-arm-restore-vms). To restore an Azure VM from an image-level backup, Veeam Backup for Microsoft Azure performs the following steps:

1. [Applies only if you perform restore from an archived backup] Retrieves data from the archived restore point.
2. [Applies only if you perform restore to the original location] Creates a staging resource group in which virtual disks of the restored Azure VM will be created, and assigns the Veeam backup appliance ID tag to the group. The tag value is the ID of the Azure VM running the backup appliance.
3. Creates empty virtual disks. The number of empty virtual disks equals the number of virtual disks attached to the source Azure VM.
4. Launches a worker instance in the Azure region where the restored Azure VM will reside, and then attaches empty virtual disks to the worker instance.
5. Restores backed-up data to the empty virtual disks on the worker instance.
6. Detaches the virtual disks with the restored data from the worker instance.
7. Deallocates the worker instance.
8. [Applies only if you perform restore to the original location] Removes the source Azure VM and the source disks from Microsoft Azure.
9. [Applies only if you perform restore to the original location] Moves the virtual disks from the staging resource group to the original resource group of the source Azure VM.
10. Creates an Azure VM in the specified location.
11. Attaches the created virtual disks with the restored data to the Azure VM.
12. [Applies only if you perform restore to the original location] Removes the staging resource group.

To learn how to restore an entire Azure VM from a cloud-native snapshot or an image-level backup, see [Performing Entire VM Restore](entire_vm_restore_ui.md).

Page updated 11/28/2025

Page content applies to build 8.0.1.202
