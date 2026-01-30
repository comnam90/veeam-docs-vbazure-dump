---
title: "Configuring Global Retention Settings"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/configuring_global_retention_settings.html"
last_updated: "4/22/2025"
product_version: "8.0.1.202"
---

# Configuring Global Retention Settings


You can configure global retention settings to specify for how long the following data will be retained in the configuration database:

* [Obsolete snapshots and replicas](#snapshots)
* [Session records](#sessions)

Configuring Retention Settings for Obsolete Snapshots

If an Azure resource (whether it is an Azure VM or an Azure file share) is no longer processed by a backup policy (for example, it was removed from the backup policy or the backup policy no longer exists), its cloud-native snapshots become obsolete. Retention policy settings configured when creating backup policies do not apply to obsolete snapshots — these snapshots are removed from the configuration database according to their own retention settings.

|  |
| --- |
| Note |
| Global retention settings apply to all cloud-native snapshots created by the Veeam backup service. If an Azure resource is still processed by a backup policy, but some of its cloud-native snapshots are older than the number of days (or months) specified in the global retention settings, these cloud-native snapshots will be removed from the configuration database. |

To configure retention settings for obsolete snapshots, do the following:

1. Switch to the Configuration page.

1. Navigate to General > Retention.

1. In the Obsolete snapshots retention section, select either of the following options:

* Select the Never option if you do not want Veeam Backup for Microsoft Azure to remove obsolete snapshots.

* Select the After option if you want to specify the number of days, months or years during which Veeam Backup for Microsoft Azure will keep obsolete snapshots in the configuration database. The number must be between 15 and 36135 for days, between 1 and 1188 for months and between 1 and 99 for years.

If you select this option, Veeam Backup for Microsoft Azure will remove obsolete instance snapshots from the configuration database as soon as the specified period of time is over.

1. Click Save.

|  |
| --- |
| Note |
| When Veeam Backup for Microsoft Azure removes an obsolete snapshot from the configuration database, it also removes the snapshot from Microsoft Azure Storage. |

Configuring Retention Settings for Session Records

Veeam Backup for Microsoft Azure stores records for the login activity and all sessions of performed data protection and disaster recovery operations in the configuration database on the additional data disk attached to the backup appliance. The default retention period for the login activity records equals 3 months and cannot be modified. The session records are removed from the configuration database according to specific retention settings.

To configure retention settings for session records, do the following:

1. In the Session retention section, select either of the following options:

* Select the Keep all sessions option if you do not want Veeam Backup for Microsoft Azure to remove session records.
* Select the Keep only last option if you want to specify the number of days, months or years during which Veeam Backup for Microsoft Azure will keep session records in the configuration database.

If you select this option, Veeam Backup for Microsoft Azure will remove all session records that are older than the specified time limit.

1. Click Save.

|  |
| --- |
| Important |
| Retaining all session records in the configuration database may overload the data disk. By default, the disk comes with 32 GB of storage capacity. If you choose not to remove sessions records at all, consider increasing the disk space to avoid runtime problems. |

[![Configuring Retention Settings](images/lingering_retention_settings.webp)](images/lingering_retention_settings.webp "Configuring Retention Settings")


