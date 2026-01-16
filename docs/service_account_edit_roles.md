---
title: "service_account_edit_roles"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/service_account_edit_roles.html"
last_updated: "8/20/2025"
product_version: "8.0.1.202"
---


In this article

At the Roles step of the wizard, you can modify the list of operations that Veeam Backup for Microsoft Azure will be able to perform using permissions of the service account:

1. Set the Enable granular role assignment toggle to On and click Edit Roles.
2. In the Management roles section, choose actions that will be performed using the service account:

* Worker management — permissions of this service account will be used to launch worker instances. If you create a service account of this type, you will be able to select it [when managing worker configurations](worker_service_account.md).
* Repository management — permissions of this service account will be used to create new repositories in target Azure blob containers and to further access the repositories during data protection and disaster recovery operations. If you create a service account of this type, you will be able to select it [when configuring repository settings](repository_ui_settings.md#Role).

|  |
| --- |
| Important |
| For Veeam Backup for Microsoft Azure to perform the selected actions using the service account, the account must be assigned the permissions listed in sections [Worker Permissions](worker_permissions.md) and [Repository Permissions](repository_permissions.md). |

1. In the Operational roles section, choose resources that will be protected using permissions of the service account, and operations that will be performed with these resources:

* If you select the Backup operation, you will be able to specify the service account when performing [VM backup](backup_chain_vm.md), [SQL backup](how_sql_backup_works.md), [Cosmos DB backup](how_cosmos_db_backup_works.md) and [virtual network configuration backup](how_vnet_backup_works.md).
* If you select the Snapshot operation, you will be able to specify the service account when performing [VM backup](snapshot_chain_vm.md) and [Azure Files backup](how_fs_backup_works.md).
* If you select the Restore operation, you will be able to specify the service account when performing [VM restore](vm_restore_hiw.md), [SQL restore](sql_restore_hiw.md), [Cosmos DB restore](cosmos_db_restore_hiw.md), [file share restore](fs_restore_hiw.md) and [virtual network configuration restore](vnet_restore_hiw.md).

  [![Editing Service Account Roles](images/edit_account_roles.webp)](images/edit_account_roles.webp "Editing Service Account Roles")

Page updated 8/20/2025

Page content applies to build 8.0.1.202
