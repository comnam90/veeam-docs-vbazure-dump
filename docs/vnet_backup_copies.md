---
title: "vnet_backup_copies"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/vnet_backup_copies.html"
last_updated: "8/20/2025"
product_version: "8.0.1.202"
---


In this article

By default, Veeam Backup for Microsoft Azure stores virtual network configuration backups in the local database. You can instruct Veeam Backup for Microsoft Azure to save additional backup copies to a repository. To do that:

1. At the Target step of the wizard, set the Enable additional copy toggle to On.
2. In the Choose repository window, select a repository that will be used to store the additional virtual network configuration backup copies.

For a backup repository to be displayed in the list of available repositories, it must be added to Veeam Backup for Microsoft Azure as described in section [Adding Backup Repositories](repository_add_ui.md) or [Adding Storage Vaults](repository_vdc_add_ui.md). The list shows only backup repositories of the Hot and Cool access tiers.

1. To save changes made to the backup policy settings, click Apply.

|  |
| --- |
| Note |
| When choosing a backup repository, consider the following:   * If you want to encrypt the backed-up virtual network configuration data, select a repository with encryption enabled. * If you want to make the backed-up virtual network configuration data immutable for the period specified in [retention settings](vnet_backup_retention.md) of the backup policy, select a repository with immutability enabled. Note that Veeam Backup for Microsoft Azure does not apply generations to virtual network configuration backups.   For more information on encryption and immutability, see [Managing Repositories](repositories.md). |

[![VNet Policy Repository Settings](images/vnet_backup_target.webp)](images/vnet_backup_target.webp "VNet Policy Repository Settings")

Page updated 8/20/2025

Page content applies to build 8.0.1.202
