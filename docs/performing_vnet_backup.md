---
title: "Performing Virtual Network Configuration Backup"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/performing_vnet_backup.html"
last_updated: "9/27/2024"
product_version: "8.0.1.202"
---

# Performing Virtual Network Configuration Backup


|  |
| --- |
| Important |
| Virtual network configuration backup is available only for backup appliances managed by a Veeam Backup & Replication server. To unlock the full functionality, you must [install Veeam Plug-in for Microsoft Azure on the server](deploying_vb.md) and [add your appliances](adding_appliance_console.md) to the backup infrastructure. |

To protect the Azure virtual network configuration and settings, Veeam Backup for Microsoft Azure comes with a preconfigured Virtual Network Configuration Backup policy. With this policy, you can protect virtual network configurations of Azure subscriptions associated with your Microsoft Entra tenants.

Veeam Backup for Microsoft Azure supports backup of the following virtual network configuration components: virtual networks, subnets, IP configurations, network security groups, route tables, network interfaces and virtual network peerings.

The Virtual Network Configuration Backup policy is disabled by default. To start protecting your Azure virtual network configuration, [edit backup policy settings](vnet_backup_edit.md) and [enable the policy](policies_disable_enable_vnet.md).

In This Section

* [Editing Virtual Network Configuration Backup Policy](vnet_backup_edit.md)
* [Enabling and Disabling Virtual Network Configuration Backup Policy](policies_disable_enable_vnet.md)
* [Starting and Stopping Virtual Network Configuration Backup Policy](policies_start_stop_vnet.md)


