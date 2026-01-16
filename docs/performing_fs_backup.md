---
title: "performing_fs_backup"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/performing_fs_backup.html"
last_updated: "4/1/2025"
product_version: "8.0.1.202"
---


In this article

One backup policy can be used to process one or more Azure file shares within one Microsoft Entra tenant. The scope of data that you can protect in a tenant is limited by permissions of a service account that is specified in the backup policy settings.

|  |
| --- |
| Important |
| Before you create an Azure Files policy, make sure the Allow storage account key access option for Shared Key authorization is enabled for the storage accounts where the file shares you plan to protect reside — otherwise, backup operations will fail. For more information on Shared Key authorization, see [Microsoft Docs](https://learn.microsoft.com/en-us/rest/api/storageservices/authorize-with-shared-key?toc=%2Fazure%2Fstorage%2Fblobs%2Ftoc.json&bc=%2Fazure%2Fstorage%2Fblobs%2Fbreadcrumb%2Ftoc.json). |

To schedule data protection tasks to run automatically, [create backup policies](fs_backup_create.md). For each protected Azure file share, you can also [take a cloud-native snapshot manually](creating_fs_snapshots_manually.md) when needed.

If you plan to receive email notifications on backup policy results, configure email notification settings first. For more information, see [Configuring Global Notification Settings](configuring_notification_settings.md).

Page updated 4/1/2025

Page content applies to build 8.0.1.202
