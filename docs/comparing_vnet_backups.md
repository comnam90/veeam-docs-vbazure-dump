---
title: "comparing_vnet_backups"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/comparing_vnet_backups.html"
last_updated: "9/16/2025"
product_version: "8.0.1.202"
---


In this article

You can compare the current Azure virtual network configuration of an Azure subscription and the virtual network configuration contained in any available restore point. To do that:

1. Navigate to Protected Data > Virtual Network.
2. Select the configuration record for an Azure subscription whose virtual network configuration you want to compare.
3. Click Compare.

By default, Veeam Backup for Microsoft Azure uses the most recent valid restore point. However, you can compare the virtual network configuration data to an earlier state. In the Compare Attributes window, click the link to the right of Restore point to select the necessary restore point.

If you want Veeam Backup for Microsoft Azure to display only backed-up virtual network configuration items that differ from the current virtual network configuration items, set the Show only changed attributes toggle to On.

[![Comparing VNet Configuration Data](images/backups_compare_vnet.webp)](images/backups_compare_vnet.webp "Comparing VNet Configuration Data")

Page updated 9/16/2025

Page content applies to build 8.0.1.202
