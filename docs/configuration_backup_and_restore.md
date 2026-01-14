---
title: "configuration_backup_and_restore"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/configuration_backup_and_restore.html"
last_updated: "9/10/2024"
product_version: "8.0.1.202"
---


In this article

You can back up and restore the configuration database that stores data collected from a backup appliance configuration for the existing backup policies, protected Azure VMs, Azure SQL databases, Cosmos DB accounts, Azure file shares, virtual network configurations, worker instance configurations, logged session records and so on. If the backup appliance goes down for some reason, you can reinstall it and quickly restore its configuration from a configuration backup. You can also use a configuration backup to migrate the configuration of one backup appliance to another appliance in Microsoft Azure.

It is recommended that you regularly perform configuration backup for every backup appliance added to the backup infrastructure. Periodic configuration backups reduce the risk of data loss and minimize the administrative overhead costs in case any problems with the backup appliance occur.

You can run configuration backup manually on demand, or instruct Veeam Backup for Microsoft Azure to do it automatically on a regular basis.

In This Section

* [Performing Configuration Backup](performing_configuration_backup.md)
* [Performing Configuration Restore](configuration_restore.md)

Page updated 9/10/2024

Page content applies to build 8.0.1.202
