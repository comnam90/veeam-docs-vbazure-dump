---
title: "Private Network Deployment"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/private_network_deployment.html"
last_updated: "9/19/2024"
product_version: "8.0.1.202"
---

# Private Network Deployment


The private deployment feature allows you to increase the security of your environment by retaining network traffic within a private network.

With Veeam Backup for Microsoft Azure, you can perform the following operations in a private environment:

* [Create image-level backups and cloud-native snapshots of Azure VMs](vm_backup_pne.md).
* [Create backups of Azure SQL databases](sql_backup_pne.md).
* [Create backups of Cosmos DB accounts](cosmos_backup_pne.md).
* [Create cloud-native snapshots of Azure file shares](fs_backup_pne.md).

When a backup appliance is deployed in a private environment, it is not assigned any public IPv4 address, and you will have to perform a number of additional configuration actions to allow private network access. For more information, see [Working in Private Environments](app_private_network.md).


