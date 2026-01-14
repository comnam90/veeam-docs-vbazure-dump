---
title: "uninstalling_vb"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/uninstalling_vb.html"
last_updated: "9/2/2025"
product_version: "8.0.1.202"
---


In this article

Starting from version 7.0, you can deploy Veeam Backup for Microsoft Azure from the Veeam Backup & Replication console only. However, if an appliance was previously deployed from the Microsoft Azure Marketplace or is running Veeam Backup for Microsoft Azure version 2.x (or earlier), perform the following steps to uninstall Veeam Backup for Microsoft Azure:

1. [Remove backed-up data](removing_backups.md).
2. [Remove IAM roles and Microsoft Entra applications used by Veeam Backup for Microsoft Azure to access Azure resources](removing_roles_apps.md).
3. [Remove Microsoft Azure resources created by Veeam Backup for Microsoft Azure](removing_resources.md).

|  |
| --- |
| Important |
| Before you uninstall the solution, remove all worker instances and created worker configurations as described in section [Managing Worker Instances](worker_instance_remove.md). |

Page updated 9/2/2025

Page content applies to build 8.0.1.202
