---
title: "repository_add_console_existing"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/repository_add_console_existing.html"
last_updated: "12/16/2025"
product_version: "8.0.1.202"
---


In this article

When you connect to a backup appliance, all repositories that have already been configured on the appliance are automatically added to the backup infrastructure.

If an existing repository is not displayed under the External Repositories node or if you have recently configured a new repository on the appliance that is already connected to the backup server, do the following:

1. In the Veeam Backup & Replication console, open the Backup Infrastructure view.
2. Navigate to Managed Servers.
3. Select a backup appliance that manages the necessary repository and click Edit Appliance on the ribbon.

Alternatively, you can right-click the backup appliance and select Properties.

1. In the Edit Veeam Backup for Microsoft Azure Appliance wizard, do the following:

1. Navigate to the Repositories step of the wizard and complete the step as described in section [Adding Appliances](adding_appliance_repository.md) (step 8).

1. Complete the Edit Veeam Backup for Microsoft Azure Appliance wizard as described in section [Adding Appliances](adding_appliance_apply.md) (steps 9-10).

Open the Backup Infrastructure view to verify that the repository is displayed under the External Repositories node.

|  |
| --- |
| Note |
| If you do not specify credentials of any Microsoft Azure storage account for a standard repository, you will only be able to use the Veeam Backup & Replication console to perform [entire VM restore](entire_vm_restore_console.md) and [SQL database restore](sql_restore_console.md) from backups stored in this repository. Moreover, information on the repository displayed in the Backup Infrastructure view under the External Repositories node will not include statistics on the amount of storage space that is currently consumed by restore points created by Veeam Backup for Microsoft Azure. |

Page updated 12/16/2025

Page content applies to build 8.0.1.202
