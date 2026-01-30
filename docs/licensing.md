---
title: "Licensing"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/licensing.html"
last_updated: "11/11/2025"
product_version: "8.0.1.202"
---

# Licensing


Veeam Backup for Microsoft Azure is licensed per protected instance. An instance is defined as a single Azure resource — an Azure VM, Azure SQL Server, Cosmos DB account or Azure file share. An instance is considered to be protected if it has a restore point (snapshot or backup) created by a backup policy during the past 31 days. Each protected instance consumes 1 license unit. However, if an instance has only manually created snapshots or backups, it does not consume any license units.

|  |
| --- |
| Note |
| Protected Azure SQL databases do not consume separate license units. If there is a number of protected databases located on a licensed Azure SQL Server, all these databases consume the license unit of this server. |

Veeam Backup for Microsoft Azure is available in 2 editions:

* Free — allows you to protect up to 10 instances free of charge. This edition applies only to backup appliances that are no longer managed by Veeam Backup & Replication servers.

Note that this edition does not support indexing of Azure Files, creating backups of Azure Virtual Network configuration components and protecting Cosmos DB accounts.

* Paid — allows you to protect the number of instances equivalent to the number of units specified in your license. This edition is licensed using the Veeam Universal License (VUL) installed on the Veeam Backup & Replication server. For more information on Veeam licensing terms and conditions, see [Veeam Licensing Policy](https://www.veeam.com/legal/licensing-policy.html#instance-conversion).

When the license expires, Veeam Backup for Microsoft Azure offers a grace period to ensure a smooth license update and to provide sufficient time to install a new license file. The duration of the grace period is 31 days after the expiration of the license. During this period, you can perform all types of data protection and disaster recovery operations. After the grace period is over, Veeam Backup for Microsoft Azure stops processing all instances and disables all scheduled backup policies. You must update your license before the end of the grace period.

|  |
| --- |
| Important |
| If you plan to use the Veeam Universal License (VUL), consider that only the Subscription license type is supported. |

If a backup appliance is managed by a Veeam Backup & Replication server, it uses the same license that is installed on this server. For more information, see [Scenarios](licensing_scenarios.md).

In This Section

* [Viewing License Information](license_view_information.md)
* [Revoking License Units](license_revoke.md)
* [Removing License](license_remove.md)


