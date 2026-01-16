---
title: "vnet_backup_subscriptions"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/vnet_backup_subscriptions.html"
last_updated: "8/2/2024"
product_version: "8.0.1.202"
---


In this article

At the Subscriptions step of the wizard, select Azure subscriptions whose virtual network configuration you want to back up.

Veeam Backup for Microsoft Azure allows you to automatically collect and back up virtual network configuration data for all Azure subscriptions selected for Azure VM, Azure SQL and Azure Files backup policies. To do that, [enable automatic protection](vnet_backup_subscriptions_automatic.md) for Azure subscriptions. To retrieve virtual network configurations of all automatically protected Azure subscriptions, Veeam Backup for Microsoft Azure will use permissions of service accounts specified in the settings of backup policies that protect resources residing in these Azure subscriptions.

You can also configure the Virtual Network Configuration Backup policy to protect configuration data for Azure subscriptions that are not specified in the settings of any backup policy, or choose another service account whose permissions Veeam Backup for Microsoft Azure will use to collect the virtual network configuration data of the automatically protected Azure subscriptions. To do that, [manually add Azure subscriptions](vnet_backup_subscriptions_manual.md) to the Virtual Network Configuration Backup policy and configure backup settings for them.

Page updated 8/2/2024

Page content applies to build 8.0.1.202
