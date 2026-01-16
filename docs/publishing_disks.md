---
title: "publishing_disks"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/publishing_disks.html"
last_updated: "12/23/2025"
product_version: "8.0.1.202"
---


In this article

Veeam Backup & Replication allows you to publish point-in-time disks, that is, to attach specific virtual disks of backed-up Azure VMs to any server to instantly access data in the read-only mode. You can copy the necessary files and folders to the target server, and perform an antivirus scan of the backed-up data. For more information, see the Veeam Backup & Replication User Guide, section [Disk Publishing (Data Integration API)](https://helpcenter.veeam.com/docs/vbr/userguide/data_integration_api.html?ver=13).

|  |
| --- |
| Important |
| Disk publishing cannot be performed using backups that are stored in [Veeam Data Cloud storage vaults](vdc_vaults.md). To perform this operation, use backups that are stored in standard backup repositories for which you have specified Microsoft Azure storage account credentials. To learn how to specify credentials for repositories, see sections [Creating New Repositories](repository_console_storage_account.md) and [Connecting to Existing Appliances](adding_appliance_repository.md). |

To publish virtual disks of an Azure VM, do the following:

1. In the Veeam Backup & Replication console, open the Home view.
2. Navigate to Backups > External Repository.
3. Expand the necessary backup policy, select the Azure VM whose disks you want to publish and click Publish Disks on the ribbon.
4. Complete the Publish Disks wizard as described in the Veeam Backup & Replication User Guide, section [Publishing Disks](https://helpcenter.veeam.com/docs/vbr/userguide/publishing_disks.html?ver=13).

[![Publishing Disks](images/disk_publishing.webp)](images/disk_publishing.webp "Publishing Disks")

Page updated 12/23/2025

Page content applies to build 8.0.1.202
