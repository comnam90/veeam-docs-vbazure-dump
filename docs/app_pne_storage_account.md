---
title: "app_pne_storage_account"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/app_pne_storage_account.html"
last_updated: "1/27/2025"
product_version: "8.0.1.202"
---


In this article

By default, Veeam Backup for Microsoft Azure uses public access to communicate with Azure storage accounts. However, you can instruct Veeam Backup for Microsoft Azure to access the storage accounts without public IPv4 addresses in the following cases:

* You want Veeam Backup for Microsoft Azure to create and manage backup repositories within a private network.
* You plan to back up unmanaged Azure VMs in a private environment.
* You plan to back up Azure Files in a private environment.

To do that, in a storage account where your repositories or resources reside, you can either [add firewall rules](app_pne_firewall.md) that will grant access to specific VNets, or [create private endpoints](app_pne_storage_endpoints.md) that will be used to connect to the resources.

Page updated 1/27/2025

Page content applies to build 8.0.1.202
