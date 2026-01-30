---
title: "File-Level Recovery"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/vm_restore_flr_hiw.html"
last_updated: "11/28/2025"
product_version: "8.0.1.202"
---

# File-Level Recovery


To recover files and folders of a backed-up Azure VM, Veeam Backup for Microsoft Azure performs the following steps:

1. Launches a worker instance in either of the following Azure regions:

* To recover files and folders from a cloud-native snapshot, the worker instance is launched in the region where the cloud-native snapshot resides.
* To recover files and folders from an image-level backup, the worker instance is launched in the region where the repository storing backed-up data resides.

1. Attaches virtual disks of the Azure VM to the worker instance.

The disks are not physically extracted from the backup — Veeam Backup for Microsoft Azure emulates their presence on the worker instance. The source backup itself remains in the read-only state.

1. [Applies only if you perform restore to the original location] Installs the Veeam restore tool on the source Azure VM.
2. Launches the file-level recovery browser.

The file-level recovery browser displays the file system tree of the backed-up Azure VM. In the browser, you can select the necessary files and folders to recover.

1. Saves the selected files and folders to the local machine, or restores the files and folders to the original Azure VM.
2. Detaches the virtual disks from the worker instance.
3. Deallocates the worker instance.

To learn how to restore individual files and folders of an Azure VM from a cloud-native snapshot or an image-level backup, see [Performing File-Level Recovery](performing_flr.md).


