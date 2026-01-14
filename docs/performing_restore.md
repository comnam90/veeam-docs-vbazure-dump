---
title: "performing_restore"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/performing_restore.html"
last_updated: "8/26/2025"
product_version: "8.0.1.202"
---


In this article

In various disaster recovery scenarios, you can perform the following restore operations using backed-up data:

* [Restore of Azure VMs](vm_restore.md) — restore Azure VMs, disks and files from cloud-native snapshots or image-level backups to the original location or to a new location.
* [Restore of Azure SQL databases](sql_restore.md) — restore Azure SQL databases from backups to the original or to a new location.
* [Restore of Cosmos DB accounts](cosmos_db_restore.md) — restore Cosmos DB accounts from restorable timestamps using native Microsoft Azure capabilities, or databases of Cosmos DB for PostgreSQL accounts from backups stored in Veeam repositories.
* [Restore of Azure Files](fs_restore.md) — restore files of file shares from cloud-native snapshots to the original location or to a new location.

* [Restore of virtual network configurations](vnet_restore.md) — restore virtual network configurations from virtual network configuration backups to the original location or to a new location.

* [Instant Recovery](performing_instant_recovery.md) — immediately restore of Azure VMs from image-level backups to VMware vSphere and Hyper-V environments, and to Nutanix AHV clusters.
* [Azure VM disk export](exporting_disks.md) — restore virtual disks and convert them to disks of the VMDK, VHD or VHDX format.
* [Azure VM disk publish](publishing_disks.md) — publish point-in-time virtual disks and copy the necessary files and folders to the target server.
* [Restore to AWS](restoring_to_amazon.md) — restore Azure VMs from image-level backups to AWS as EC2 instances.
* [Restore to Google Cloud](restoring_to_google.md) — restore Azure VMs from image-level backups to Google Cloud as VM instances.
* [Restore to Nutanix AHV](restoring_to_nutanix.md) — restore Azure VMs from image-level backups to Nutanix AHV as Nutanix AHV VMs.

|  |
| --- |
| Note |
| You can perform all recovery operations using restore points stored in standard repositories. For restore points stored in archive repositories, only restore of Azure VMs, Azure SQL databases, databases of Cosmos DB for PostgreSQL accounts and databases and collections of Cosmos DB for MongoDB accounts to Microsoft Azure is supported. |

Page updated 8/26/2025

Page content applies to build 8.0.1.202
