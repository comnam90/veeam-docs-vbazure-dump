---
title: "Managing Backed-Up Data Using Web UI"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/managing_backups_ui.html"
last_updated: "9/27/2024"
product_version: "8.0.1.202"
---

# Managing Backed-Up Data Using Web UI


Veeam Backup for Microsoft Azure stores information on all protected Azure resources in the configuration database. Even if a resource is no longer protected by any configured backup policy and even if the resource no longer exists in Microsoft Azure, information on the backed-up data will not be deleted from the database until Veeam Backup for Microsoft Azure automatically removes all restore points associated with this resource according to the retention settings saved in the backup metadata. You can also remove the restore points manually on the Protected Data page.

|  |
| --- |
| Note |
| Veeam Backup for Microsoft Azure does not include restore points created manually in backup and snapshot chains, and does not apply the configured retention policy settings to these restore points. This means that the restore points are kept in your Microsoft Azure environment unless you remove them manually, as described in sections [Removing VM Backups and Snapshots](removing_vm_backups_and_snapshots.md), [Removing SQL Backups](removing_sql_backups.md), [Removing Cosmos DB Backups](removing_cosmos_db_backups.md), [Removing File Share Snapshots](removing_fs_snapshots.md) and [Removing Virtual Network Configuration Backups](removing_vnet_backups.md). |

In This Section

* [Azure VM Data](managing_vm_data.md)
* [Azure SQL Data](managing_sql_data.md)
* [Cosmos DB Data](managing_cosmos_db_data.md)
* [Azure Files Data](managing_azure_files.md)
* [Virtual Network Configuration Data](managing_vnet_data.md)


