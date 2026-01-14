---
title: "entire_vnet_restore_hiw"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/entire_vnet_restore_hiw.html"
last_updated: "3/26/2024"
product_version: "8.0.1.202"
---


In this article

To restore the entire virtual network configuration from a backup, Veeam Backup for Microsoft Azure performs the following steps:

1. Retrieves the backed-up virtual network configuration from the Veeam Backup for Microsoft Azure database.
2. Validates the restore operation: sends API requests to Microsoft Azure to verify that Azure service quotas are not exceeded and there are no subnet CIDR block conflicts.
3. Retrieves information on existing items and their settings in the current Azure virtual network configuration.
4. Restores the backed-up virtual network configuration:

1. Creates the missing virtual network configuration items.
2. Modifies settings of the existing items that do not match the backed-up settings.

To learn how to restore the entire virtual network configuration from a virtual network configuration backup, see [Performing Entire Virtual Network Configuration Restore](entire_vnet_restore.md).

Page updated 3/26/2024

Page content applies to build 8.0.1.202
