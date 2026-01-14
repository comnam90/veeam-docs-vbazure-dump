---
title: "repositories"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/repositories.html"
last_updated: "8/20/2025"
product_version: "8.0.1.202"
---


In this article

Veeam Backup for Microsoft Azure uses blob containers as target locations for image-level backups of Azure VMs, backups of Azure SQL databases Cosmos DB for PostgreSQL accounts and Cosmos DB for MongoDB accounts, and backup copies of virtual network configurations. To store backups in blob containers, configure repositories. Veeam Backup for Microsoft Azure version 8.1 comes with 2 types of repositories:

* Backup repository — a folder created by Veeam Backup for Microsoft Azure in a blob container that resides in a specific Azure storage account managed by Azure users in Microsoft Azure.
* Storage vault — a folder created by Veeam Backup for Microsoft Azure in a blob container that resides in a specific Azure storage account managed by Veeam in Veeam Data Cloud Vault.

|  |
| --- |
| Important |
| A repository must not be managed by multiple backup appliances simultaneously. Retention sessions running on different appliances may corrupt backups stored in the repository, which may result in unpredictable data loss. |

In This Section

* [Adding Backup Repositories Using Console](repository_add_console.md)
* [Adding Backup Repositories Using Web UI](repository_add_ui.md)
* [Adding Storage Vaults Using Web UI](repository_vdc_add_ui.md)
* [Editing Repository Settings](repository_edit.md)
* [Rescanning Repositories](repository_rescan.md)
* [Removing Repositories](repository_remove.md)

Page updated 8/20/2025

Page content applies to build 8.0.1.202
