---
title: "Creating SQL Backup Policies"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/sql_backup_create.html"
last_updated: "2/18/2025"
product_version: "8.0.1.202"
---

# Creating SQL Backup Policies


|  |
| --- |
| Important |
| SQL backup policies can protect only Azure SQL databases running on SQL Servers and databases located on SQL Managed Instances. If you want to protect a database hosted by a SQL Server on Azure VM, create an [Azure VM backup policy](performing_vm_backup.md). Note that in this case, you will not be able to restore a single database without restoring the entire VM. |

To create a backup policy, do the following:

1. [Launch the Add Azure SQL Policy wizard](sql_backup_wizard.md).
2. [Specify a backup policy name and description](sql_backup_name.md).
3. [Configure backup source settings](sql_backup_source_settings.md).
4. [Configure processing options](sql_processing_options.md).
5. [Create a schedule for the backup policy](sql_backup_policy_schedule.md).
6. [Specify automatic retry, health check and notification settings for the backup policy](sql_backup_retry_notifications.md).
7. [Review the estimated cost of protecting the selected Azure SQL databases](sql_backup_cost.md).
8. [Finish working with the wizard](sql_backup_finish.md).


