---
title: "service_accounts"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/service_accounts.html"
last_updated: "9/27/2024"
product_version: "8.0.1.202"
---


In this article

For each data protection and disaster recovery operation performed for an Azure resource, you must specify a service account that has access to the resource and a set of permissions that determine what operations are allowed for the resource.

Particularly, Veeam Backup for Microsoft Azure uses service accounts to perform the following tasks:

* To enumerate resources added to backup policies.

* To create snapshots and backups of Azure resources protected by policies.
* To create and manage worker instances.
* To create and manage backup repositories.
* To attach virtual disks to worker instances when performing image-level backup.
* To restore Azure VMs, virtual disks, and files and folders from cloud-native snapshots and image-level backups.
* To restore Azure SQL databases and Cosmos DB accounts from backups.
* To restore files of Azure file shares from cloud-native snapshots.
* To create backups of Azure virtual network configurations.
* To restore backups of Azure virtual network configurations from backups.

In This Section

* [Adding Service Accounts](service_account_add.md)
* [Editing Service Accounts](service_account_edit.md)
* [Checking Service Account Permissions](service_account_check.md)
* [Removing Service Accounts](service_account_remove.md)

Page updated 9/27/2024

Page content applies to build 8.0.1.202
