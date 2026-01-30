---
title: "Performing File Share Restore Using Web UI"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/performing_fs_restore_ui.html"
last_updated: "4/1/2025"
product_version: "8.0.1.202"
---

# Performing File Share Restore Using Web UI


In case a disaster strikes, you can recover corrupted or missing files of an Azure file share from a cloud-native snapshot. Veeam Backup for Microsoft Azure allows you to restore files and folders to the original file share or to another file share.

|  |
| --- |
| Important |
| The Allow storage account key access option for Shared Key authorization must be enabled for both the storage accounts where the protected file shares reside and the storage accounts where the file shares to which you plan to restore files and folders reside — otherwise, the restore operation will fail. For more information on the Shared Key authorization, see [Microsoft Docs](https://learn.microsoft.com/en-us/rest/api/storageservices/authorize-with-shared-key?toc=%2Fazure%2Fstorage%2Fblobs%2Ftoc.json&bc=%2Fazure%2Fstorage%2Fblobs%2Fbreadcrumb%2Ftoc.json). |

How to Perform File Share Restore

To restore files and folders of a protected Azure file share, do the following:

1. [Launch Azure Files File-Level Recovery wizard](fs_restore_ui_wizard.md).
2. [Select a service account](fs_restore_ui_service_account.md).
3. [Choose a restore mode](fs_restore_ui_mode.md).
4. [Specify a restore reason](fs_restore_ui_reason.md).
5. [Finish working with the wizard — start a recovery session](fs_restore_ui_start.md).
6. [Select a restore point](fs_restore_ui_point.md).
7. [Choose files and folders to restore](fs_restore_ui_items.md).
8. [Stop the restore session](fs_restore_ui_stop.md).


