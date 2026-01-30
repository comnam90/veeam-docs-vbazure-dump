---
title: "Upgrading Appliances"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/upgrading_appliances_ui.html"
last_updated: "1/29/2026"
product_version: "8.0.1.202"
---

# Upgrading Appliances


Starting from Veeam Backup for Microsoft Azure version 5a, you can upgrade backup appliances from the Veeam Backup & Replication console only. Direct upgrade to Veeam Backup for Microsoft Azure version 8.1 is supported from Veeam Backup for Microsoft Azure version 6.0 or 7.0. To upgrade from an earlier version, you must first [upgrade to Veeam Backup for Microsoft Azure version 6.0 or 7.0](https://helpcenter.veeam.com/archive/vbazure/70/guide/upgrading_appliances_console.html).

|  |
| --- |
| Important |
| * Before you upgrade a backup appliance, make sure that all backup policies are both disabled and stopped, and no restore tasks are currently executing. Otherwise, the update process will interrupt the running activities, which may result in data loss. * If your backup appliance used the Azure Service Bus messaging service in versions prior to version 8.1, you must switch to the Azure Queue Storage service immediately after you upgrade to version 8.1. Otherwise, Veeam Backup for Microsoft Azure will no longer be able to perform backup and restore operations. For more information, see [Configuring Deployment Mode](deployment_mode.md). |

To upgrade a backup appliance, do the following:

1. Install Veeam Plug-in for Microsoft Azure as described in section [Deployment](deploying_vb.md).

If you do not have a valid Veeam Backup & Replication license, you can download a [30-day trial version](https://www.veeam.com/backup-replication-vcp-download.html) of the product.

1. Add the backup appliance to the Veeam Backup & Replication infrastructure as described in section [Connecting to Existing Appliances](connecting_appliance_console.md).

When connecting to the backup appliance, Veeam Backup & Replication will display a warning notifying you that the appliance must be upgraded. Acknowledge the warning to allow Veeam Backup & Replication to automatically upgrade the appliance to the necessary version.

|  |
| --- |
| Note |
| When you add a backup appliance to the Veeam Backup & Replication infrastructure, the license installed on the appliance becomes invalid. Protected instances start consuming license units from the license installed on the Veeam Backup & Replication server. However, as soon as you remove the backup appliance from the Veeam Backup & Replication infrastructure, Veeam Backup for Microsoft Azure will continue using the license that had been used before you added the backup appliance to the Veeam Backup & Replication infrastructure.  For more information on licensing scenarios, see [Licensing](licensing.md). |

1. [Applies only if the backup appliance has not been upgraded at step 2] Upgrade the appliance as described in section [Updating Appliances Using Console](updating_console.md).
2. After the upgrade process completes, you can remove the backup appliance from the Veeam Backup & Replication infrastructure, as described in section [Removing Appliances](removing_appliance_console.md), if you do not plan to further manage this appliance from the Veeam Backup & Replication console.

Make sure to remove the appliance from the Veeam Backup & Replication infrastructure before you uninstall Veeam Backup & Replication. Otherwise, Veeam Backup for Microsoft Azure will not be able to perform backup and restore operations due to the licensing issues.

If you remove the backup appliance from the backup infrastructure, you will no longer be able to create backups of virtual network configurations and Cosmos DB accounts. For more information, see [Integration with Veeam Backup & Replication](integration_vbr.md).

Related Topics

[Checking for Updates](updates_check.md)


